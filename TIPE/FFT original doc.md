Implementing complex numbers and FFT with just datatypes (no floats)
--------------------------------------------------------------------

In this article, I'll explain why implementing numbers with just algebraic
datatypes is desirable. I'll then talk about common implementations of FFT (Fast
Fourier Transform) and why they hide inherent inefficiencies. I'll then show how
to implement integers and complex numbers with just algebraic datatypes, in a
way that is extremely simple and elegant. I'll conclude by deriving a pure
functional implementation of complex FFT with just datatypes, no floats.

Why implement numbers with ADTs?
--------------------------------

For most programmers, "real numbers" are a given: they just use floats and call
it a day. But, in some cases, it doesn't work well, and I'm not talking about
precision issues. When trying to prove statements on real numbers in proof
assistants like Coq, we can't use doubles, we must formalize reals using
datatypes, which can be very hard. For me, the real issue arises when I'm trying
to implement optimal algorithms on [HVM](https://github.com/higherorderco/hvm).
To do that, I need functions to fuse, which is a fancy way of saying that `(+ 2)
.  (+ 2)` "morphs into" `(+ 4)` during execution - yet, machine floats block
that mechanism. Because of that, I've been trying to come up with an elegant way
to implement numbers with just datatypes. For natural numbers, it is easy: we
can just implement them as bitstrings:

```haskell
-- O stands for bit 0
-- I stands for bit 1
-- E stands for end-of-string
data Nat = O Nat | I Nat | E deriving (Show)

-- Applies 'f' n times to 'x'.
rep :: Nat -> (a -> a) -> a -> a
rep (O x) f = rep x (\x -> f (f x))
rep (I x) f = rep x (\x -> f (f x)) . f
rep E     f = id

-- Increments a Nat.
inc :: Nat -> Nat
inc E     = O E
inc (O x) = I x
inc (I x) = O (inc x)

-- Adds two Nats.
add :: Nat -> Nat -> Nat
add a = rep a inc

main :: IO ()
main = do
  let a = I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I (I E)))))))))))))))))))))))))
  let b = O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O (O E)))))))))))))))))))))))))
  print (add a b)
```

The program above implements addition by repeated increment, and is the simplest
numerical example where fusion makes a big difference, being exponential on
Haskell and [linear on HVM](https://gist.github.com/VictorTaelin/4a537342ee3c33f56fc3c374946e7fbb). But this isn't useful in practice, as we already have
fast addition algorithms like add-carry. The question, then, becomes: is it possible to explore
optimality to implement numeric algorithms that actually beat existing ones in
practice? The idea is that we could implement numbers with datatypes, which are, usually,
much slower than floats, but, if the resulting asymptotics are improved,
then this would easily pay off. One of the most successful numeric algorithms ever is the FFT. How
would an "optimal FFT" look like? Let's find out!

What is wrong with the textbook FFT
-----------------------------------

Designing optimal functions is extremely tricky, because it takes very little to
interrupt fusion and get an exponential slowdown. For example, if we change the
`inc` Haskell function above to let the Nat grow in size:

```haskell
inc :: Nat -> Nat
inc E     = I E -- allows the bitstring to grow
inc (O x) = I x
inc (I x) = O (inc x)
```

Then, the fact we're now using the "I" constructor twice will prevent us from
fusing the corresponding function on the HVM. A single character will downgrade
it from linear to exponential! There are bazillion ways to ruin fusion. Passing
a state as an argument, placing a lambda in the wrong location, using an
argument more than once... in fact, it feels like anything that detours from a
"direct linear recursion" will refuse to fuse. With that in mind, let's examine
the textbook FFT:

*Note: you do not need to understand FFT to read this article - just view this as
a random snippet we want to optimize.*

```haskell
-- FFT receives a polynomial P, represented as a list of complex coefficients,
-- and returns the evaluation of P on len(P) points of the unit circle. Example:
-- - input  = [A,B,C,D,E,F,G,H]
-- - output = [P(e(0/8)),P(e(1/8)),P(e(2/8)),P(e(3/8)),P(e(4/8)),P(e(5/8)),P(e(6/8)),P(e(7/8))]
--          where P(x) = A + Bx¹ + Cx² + Dx³ + Ex⁴ + Fx⁵ + Gx⁶ + Hx⁷
--                e(x) = e^(2πxi)

-- When len=1, we must eval P(e^(0*2πi)) where P(x) = A. That's just A.
fft [x] = [x]

-- When len>1...
fft xs = pts where

  -- If len=8, we'll eval P = A + Bx¹ + Cx² + Dx³ + Ex⁴ + Fx⁵ + Gx⁶ + Hx⁷
  -- on x ∈ [e(0/8),e(1/8),e(2/8),e(3/8),e(4/8),e(5/8),e(6/8),e(7/8)]
  len = length xs

  -- We first split it on two polynomials, based on even/odd exponents:
  eve = split 0 xs -- EVE = A   + Cx² + Ex⁴ + Gx⁶
  odd = split 1 xs -- ODD = Bx¹ + Dx³ + Fx⁵ + Hx⁷

  -- We then call FFT recursively on EVE and ODD
  pt0 = fft eve -- PT0 = A + Cx¹ + Ex² + Gx³ evaluated on x ∈ [0/4𝜏,1/4𝜏,2/4𝜏,3/4𝜏] (by induction)
                -- PT0 = A + Cx² + Ex⁴ + Gx⁶ evaluated on x ∈ [0/8𝜏,1/8𝜏,2/8𝜏,3/8𝜏] (by equivalence)
  pt1 = fft odd -- PT1 = B + Dx¹ + Fx² + Hx³ evaluated on x ∈ [0/4𝜏,1/4𝜏,2/4𝜏,3/4𝜏] (by induction)
                -- PT1 = B + Dx² + Fx⁴ + Hx⁶ evaluated on x ∈ [0/8𝜏,1/8𝜏,2/8𝜏,3/8𝜏] (by equivalence)

  -- We then compute e(x) for each angle, which are the "twiddle factors"
  twi = [cPol (2 * pi * fromIntegral k / fromIntegral len) | k <- [0..len `div` 2 - 1]]

  -- We then multiply PT1 by the tiddle factors
  pt2 = zipWith cMul twi pt1 -- PT2 = Bx¹ + Dx³ + Fx⁵ + Hx⁷ evaluated on x ∈ [0/8𝜏,1/8𝜏,2/8𝜏,3/8𝜏]

  -- Finally, we obtain all points as PT0 +- PT2
  -- This exploits the symmetry of polynomials
  ptl = zipWith cAdd pt0 pt2 -- PTL = A + Bx¹ + Cx² + Dx³ + Ex⁴ + Fx⁵ + Gx⁶ + Hx⁷ evaluated on [0/8𝜏,1/8𝜏,2/8𝜏,3/8𝜏]
  ptr = zipWith cSub pt0 pt2 -- PTR = A + Bx¹ + Cx² + Dx³ + Ex⁴ + Fx⁵ + Gx⁶ + Hx⁷ evaluated on [4/8𝜏,5/8𝜏,6/8𝜏,7/8𝜏]

  -- The result just combines PTL and PTR to get all unit circle points
  pts = ptl ++ ptr
```

[Complete code.](https://gist.github.com/VictorTaelin/7a7aba09275f88d159d9fb3ecf948860)

So, what is wrong with this? Well, when it comes to optimality, everything.
First, it traverses the list just to compute its length. Then, it copies the
entire list 2 more times to split even/odd indices. Then, it traverses the odds
list twice. Then it copies it. Then it re-generates the same twiddle factors
over and over. Then it traverses everything a few more times with zips. All
these things block fusion, and, if that wasn't bad enough, it performs
arithmetic on machine floats on its its inner loop, which removes any remaining
hope we could have. So, how can it be improved?

Improving the structure of FFT
------------------------------

The first insight is to replace lists by balanced binary trees, and store
elements on nodes such that, by starting from any element of the tree, walking
up to the root, and annotating the branches we passed through as 0 for left and
1 for right, we'll get the binary representation of the index. For example:

```
[0, 1, 2, 3, 4, 5, 6, 7]
```

Is represented as:

```
(B (B (B (L 0) (L 4)) (B (L 2) (L 6))) (B (B (L 1) (L 5)) (B (L 3) (L 7))))
```

If we start from `6`, and move up until the root, we'll pass through right
(`1`), right (`1`) and left (`0`) branches of a node, which agrees with the fact
`110` is `6` in binary.

Storing elements that way has two benefits. First, we can now split a tree into
even/odd indices in O(1) by just taking the left/right branches, removing the no
need to call the "split" function, which is O(N), on every recursive call. For
example, by taking the left branch of that tree, we get:

```
(B (B (L 0) (L 4)) (B (L 2) (L 6)))
```

Which corresponds to the list `[0, 2, 4, 6]`, i.e., the even indices of the
original list. And if we take the left branch again, we get:

```
(B (L 0) (L 4))
```

Which corresponds to the list `[0, 4]`, which is, once again, the even indices
of the list above. The second benefit is that we're now able to replace the 3
calls to `zipWith` by a single call to `mix`, which combines `evens`, `odds` and
the twiddle factors in a single pass. Here is the improved version:

```haskell
data Complex = C Double Double deriving Show
data Nat     = E | O Nat | I Nat deriving Show
data Tree a  = L a | B (Tree a) (Tree a) deriving Show

fft :: Nat -> Tree Complex -> Tree Complex
fft ang (B eve odd) =
  let pt0 = fft (O ang) eve
      pt1 = fft (O ang) odd
  in mix ang pt0 pt1
fft ang (L x) = L x

mix :: Nat -> Tree Complex -> Tree Complex -> Tree Complex
mix ang (B ax ay) (B bx by) =
  let ptl = mix (O ang) ax bx
      ptr = mix (I ang) ay by
  in B ptl ptr
mix ang (L pt0) (L pt1) =
  let pt2 = cMul pt1 (cPol (2 * pi * natVal ang 0 / 2 ** fromIntegral (natLen ang + 1)))
      ptl = L (cAdd pt0 pt2)
      ptr = L (cSub pt0 pt2)
  in B ptl ptr
```

[Complete code.](https://gist.github.com/VictorTaelin/fe57adcf7c4687922cc7c0aa716bf722)

The way it works is similar, with all unnecessary work removed. The `fft` function
receives a tree with coefficients, and calls itself recursively on the left and
right branches, which corresponds to even and odd coefficients on the original
polynomial. Then, it combines the set of recursive points in a single pass by
calling the `mix` function. Finally, it doesn't generate a list of twiddle
factors. Instead, it stores an angle (as a natural number, ranging from `0` to
`N`, where `N` is the number of points) which is then used to generate the
twiddle factor at the bottom of the recursion.

While this algorithm is less pedagogical and readable, it is fully linear and
way less contrived for the runtime. It is in a healthy shape for optimality, but
there is still a problem: it represents complex numbers using floats, thus
requires machine numbers that don't fuse. Of course, we could perform FFT over
other fields, but in some cases we really need complex FFT.

Implementing integers with datatypes
------------------------------------

Our ultimate goal is to come up with an implementation of `Complex` that can be
used on FFT, and that is based purely on ADTs, i.e., no native floats, in such a
way that is simple and direct enough to possibly fuse. Let's begin with a
simpler goal: integers. Let's recall how we implemented `Nat` and `inc`:

```haskell
data Nat = O Nat | I Nat | E deriving (Show)

inc :: Nat -> Nat
inc E     = O E
inc (O x) = I x
inc (I x) = O (inc x)
```

So, what about `Int`? We could try implementing it by using a `Nat` and a sign:

```haskell
-- sign = True  correspond to  0,  1,  2,  3, ...
-- sign = False correspond to -1, -2, -3, -4, ...
data Int = Int Bool Nat

intInc :: Int -> Int
intInc (Int True  n) = Int True (inc n)
intInc (Int False n)
    | isMinusOne n = Int True natZero
    | otherwise    = Int False (dec n)
```

But this is actually a bad idea since, by pattern-matching on the boolean to
treat cases separately we inhibit fusion. Also, calling `isMinusOne` makes it
non-linear, which also inhibits fusion. In general, this is exactly the shape of
code that does not fuse. We're looking for something more uniform, that doesn't
separate the sign.

Fortunatelly, there is a pretty elegant way to do it: [balanced
ternary](https://en.wikipedia.org/wiki/Balanced_ternary). It is similar to
ternary numbers, expect its digits are not `0,1,2`, but `-1,0,1`. The `-1` digit
is usually written as `T`, so, for example, the string `11T` represents `9 + 3 -
1`, which is `11`. Amazingly, all integers can be uniquely represented in this
system. Let's count:

```
num   trits
--- | -----
−13 |   𝖳𝖳𝖳
−12 |   𝖳𝖳0
−11 |   𝖳𝖳1
−10 |   𝖳0𝖳
 −9 |   𝖳00
 −8 |   𝖳01
 −7 |   𝖳1𝖳
 −6 |   𝖳10
 −5 |   𝖳11
 −4 |    𝖳𝖳 
 −3 |    𝖳0
 −2 |    𝖳1
 −1 |     𝖳
  0 |     0
  1 |     1
  2 |    1𝖳
  3 |    10
  4 |    11
  5 |   1𝖳𝖳
  6 |   1𝖳0
  7 |   1𝖳1
  8 |   10𝖳
  9 |   100
 10 |   101
 11 |   11𝖳
 12 |   110
 13 |   111
```

Beautiful, isn't it? Its symmetric proporties and simple arithmetic are
quite important for fusion. Here is an implementation of `Int` and `inc`:

```haskell
-- T stands for digit -1
-- O stands for digit  0
-- I stands for digit  1
-- E stands for end-of-string
data Int = T Int | O Int | I Int | E

inc :: Int -> Int
inc E     = E
inc (T x) = O x
inc (O x) = I x
inc (I x) = t (Inc x)
```

As you can imagine, this representation of `Int`, and its arithmetic operations,
can be implemented on HVM in a way that fuses nicely, solving part of the
problem. But what about real and complex numbers? 

Implementing complex numbers with datatypes
-------------------------------------------

Sadly, it took me a long time to figure out the proper way to do `Int`, which is
astronomically simpler than these. Just to think of the complexity of floats
(which include sign, mantissa, exponent, NaNs...), Dedekind Cuts, Cauchy
Sequences and the like would give us the feeling we'll never find a
representation of real numbers that is as nice and uniform as the `Int` type
above. Yet, for the sake of FFT, there is some light at the end of the tunnel.

The insight is that we don't actually need all complex numbers; we just need
enough of them to represent roots of unity. In fact, if we wanted to perform FFT
on lists of 2 elements, integers would be enough for us, since we only need to
evaluate polynomials on 2 complex points, `[1, -1]`, which are both just ints!

![G0](https://i.imgur.com/LLKtBme.png)

But what if there were 4 elements? In this case, we would actually need 4
points: `[1, i, -1, -i]`... which is beyond the set of integers. But there is an
common extension of integers that could help: [Gaussian
Integers](https://en.wikipedia.org/wiki/Gaussian_integer), which add the square
root of `-1`, `i`, to `Int`. It forms sort of a quantized grid over the complex
plane, as follows:

![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Gaussian_integer_lattice.svg/1200px-Gaussian_integer_lattice.svg.png)

We could implement that type as follows:

```haskell
-- Represents (A + B*i)
data Gauss = G Int Int
```

This would give us 4 roots of unity, and, thus, the ability to perform FFT on
lists of 4 elements!

![](https://i.imgur.com/Fp6aZm4.png)

What about 8 elements though? Well, the idea here is to simply keep going, and
add a new constant, `j`, which is the square root of `i`. Once we do that, we
need 4 ints to represent a number; that's because `ij` is also part of the set,
so any number can be represented as `A + B*i + C*j + D*ij`. We can implement
this extended Gaussian Integer as:

```haskell
-- Represents (A + B*i + C*j + D*ij)
data ExtGauss = G Int Int Int Int
```

This would give us 8 roots of unity, and, thus, the ability to perform FFT on
lists of 8 elements.

![](https://i.imgur.com/j16xxSD.png)

And it would allow us to represent "fractional" complex numbers with just
integers. For example, the number `4.652 + 7.816 * i` can be approximated as
`1 + 2*i + 3*j + 4*ij`, which can be constructed as:

```
num :: ExtGauss
num = G 1 2 3 4
```

As you can see, we can keep going and generalize this to make the set `G(N)`,
with `G(0)` being Integers, `G(1)` being Gaussian Integers, `G(2)` being
Extended Gaussian Integers, and so on. To implement it, we can use a tree:

```haskell
data Tree a = V a | B (Tree a) (Tree a)
type GN     = Tree Int
```

For `G(3)`, we have 16 roots of unity, and can perform FFT on lists of 16 elements:

![](https://i.imgur.com/MaSgTh2.png)

To add two complex numbers of `GN`, we just do so pairwise:

```haskell
add :: GN -> GN -> GN
add (L z)   (L w)   = L (z + w)
add (B a b) (B c d) = B (add a c) (add b d)
```

But what about multiplication? A very elegant algorithm, [found by
T6](https://discord.com/channels/912426566838013994/1007033260662071306/1102709697435418715)
on HOC's discord, allows us to multiply a GN number by bases like `i`, `j`, `k`,
etc., with just rotations and negation:

```haskell
rot :: GN -> GN
rot (L z)   = L (-z)
rot (B a b) = B (rot b) a
```

This simple function, if applied on a `GN` element, will multiply it by its
smallest base. So, for example, on `G(3)`, rot performs multiplication by `k`.
On `G(2)`, it multiplies by `j`. On `G(1)`, it multiplies by `i`. On `G(0)`,
which is just a scalar, it negates the number. Very nice! We can use `Rot` to
multiply two `GN` elements as follows (once again, thanks T6):

```haskell
mul :: GN -> GN -> GN
mul (L z)   (L w)   = L (z * w)
mul (B a b) (B c d) = B (add (mul a c) (rot (mul b d))) (add (mul b c) (mul a d))
```

Which is, again, very elegant. But, for the sake of FFT, we don't actually need
to perform multiplication of two arbitrary numbers during the algorithm; we just
need to multiply by twiddle factors on the upper side of the unit circle. As
such, we can use this simplified algorithm, which receives an angle on the unit
circle, represented by a Nat, and multiplies it by the respective point:

```haskell
mul :: Nat -> GN -> GN
mul E     x         = x
mul (O p) (L x)     = id  (L x)
mul (I p) (L x)     = rot (L x)
mul (O p) (B ax ay) = id  (B (mul p ax) (mul p ay))
mul (I p) (B ax ay) = rot (B (mul p ax) (mul p ay))
```

So, for example, `mul (I (I (I E))) x` will multiply `x` by `ijk`, which is
approximately `-0.923 + 0.382i`. This completely removes the need for computing 
`cos`, `sin`, `e^ix`, and the like, simplifying the `pt2` computation from:

```haskell
pt2 = cMul pt1 (cPol (2 * pi * natVal ang 0 / 2 ** fromIntegral (natLen ang + 1)))
```

To just:

```haskell
let pt2 = mul (ang E) pt1
```

In other words, all the complex floating point arithmetic, including
trigonometric and exponentiation functions, are replaced by the `mul` function
above, which is just a simple recursive pass over the tree structure!

Implementing FFT with datatypes
-------------------------------

After all this, we're finally able to implement a complete FFT algorithm, in 40
lines of Haskell code, with just plain ADTs:

```haskell
data Nat    = E | O Nat | I Nat
data Tree a = L a | B (Tree a) (Tree a)
type GN     = Tree Int

add :: GN -> GN -> GN
add (L x)     (L y)     = L (x + y)
add (B ax ay) (B bx by) = B (add ax bx) (add ay by)

sub :: GN -> GN -> GN
sub (L x)     (L y)     = L (x - y)
sub (B ax ay) (B bx by) = B (sub ax bx) (sub ay by)

rot :: GN -> GN
rot (L z)   = L (-z)
rot (B x y) = B (rot y) x

mul :: Nat -> GN -> GN
mul E     x         = x
mul (O p) (L x)     = L x
mul (I p) (L x)     = rot (L x)
mul (O p) (B ax ay) = B (mul p ax) (mul p ay)
mul (I p) (B ax ay) = rot (B (mul p ax) (mul p ay))

fft :: (Nat -> Nat) -> Tree GN -> Tree GN
fft ang (L x)   = L x
fft ang (B x y) =
  let pt0 = fft (ang.O) x
      pt1 = fft (ang.O) y
  in mix ang pt0 pt1

mix :: (Nat -> Nat) -> Tree GN -> Tree GN -> Tree GN
mix ang (B ax ay) (B bx by) =
  let ptl = mix (ang.O) ax bx
      ptr = mix (ang.I) ay by
  in B ptl ptr
mix ang (L pt0) (L pt1) =
  let pt2 = mul (ang E) pt1
      ptl = L (add pt0 pt2)
      ptr = L (sub pt0 pt2)
  in B ptl ptr
```

Yes, this the a complete implementation! Note in this version I'm actually using
the primitive Haskell `Int`, but, as we've stablished, it can be implemented
with just ADTs via balanced ternary.
[Here](https://gist.github.com/VictorTaelin/af471e66a03a9a3efca25a42f6376aae) is
a complete Haskell file which performs FFT using GNs, with some helper functions
to convert it from and to lists of normal complex numbers, for visualization.

So, how does this behave on the HVM? I don't know. I've just finished
implementing it on Haskell and will spend some time trying to adjust it for the
HVM in the future. There are many things to tweak. For example, `sub` isn't
necessary and can easily be removed; Nat angles can be replaced by a twiddle
multiplier; `mix` could be simplified, perhaps. But, as is, this gets rid of
most of the inefficiencies with common FFT, and, as far as I know, is the
cleanest version of FFT in a pure functional sense. If you like it, feel
encouraged to join the [Higher Order
Community](http://discord.higherorderco.com/) to talk about it and ask any
questions. Thanks for reading!

Edit: read the comments below for a cool surprise :)