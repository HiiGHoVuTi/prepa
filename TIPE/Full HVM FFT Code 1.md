```js
(IZ)   = λs λz z
(IS n) = λs λz (s (n s z))
(IO f) = λs λz let g = (f s); (g (g z))
(II f) = (IS (IO f))
(IN 0) = IZ
(IN s) = (IS (IN (- s 1)))

Z     = λz λs z
(S n) = λz λs (s n)
(N 0) = Z
(N s) = (S (N (- s 1)))
(A s) = (s λb(b) λpλb(S ((A p) b)))

T = λt λo λi t
O = λt λo λi o
I = λt λo λi i

//G : ℕ → Set
//G  Z    = ℤ
//G (S p) = C (G p) (G p)
(C ax ay) = λc (c ax ay)

// Zero : ∀ n → G n
(Zero n) =
  let case_zero = λtλoλi(o)
  let case_succ = λp (let z = (Zero p); (C z z))
  (n case_zero case_succ)

// All : ∀ n → G n
(All n) =
  let case_zero = λtλoλi(i)
  let case_succ = λp (let a = (All p); (C a a))
  (n case_zero case_succ)

// Unit : ∀ n → G n
(Unit s) =
  let case_zero = λtλoλi(i)
  let case_succ = λp (C (Unit p) (Zero p))
  (s case_zero case_succ)

// Rot : ∀ n -> G n -> G n
(Rot s a) =
  let case_zero = λa λtλoλi(a i o t)
  let case_succ = λp λa λc (a λax λay (c (Rot p ay) ax))
  (s case_zero case_succ a)

// IRot : ∀ n -> G n -> G n
(IRot s a) =
  let case_zero = λa λtλoλi(a i o t)
  let case_succ = λp λa λc (a λax λay (c ay (IRot p ax)))
  (s case_zero case_succ a)

// Neg : ∀ n -> G n -> G n
(Neg s a) =
  let case_zero = λa λtλoλi(a i o t)
  let case_succ = λp λa λc (a λax λay (c (Neg p ax) (Neg p ay)))
  (s case_zero case_succ a)

// Add : ∀ n -> G n -> G n -> G n
(Add s a b) =
  let case_zero = λa λb (a λbλtλoλi(b i t o) λb(b) λbλtλoλi(b o i t) b)
  let case_succ = λp λa λb λc (a λax λay (b λbx λby
    let cx = (Add p ax bx)
    let cy = (Add p ay by)
    (c cx cy)))
  (s case_zero case_succ a b)

// mul : ∀ n -> G n -> G n -> G n
(Mul s a b) =
  let case_zero = λa λb (a λbλtλoλi(b i o t) λbλtλoλi(o) λb(b) b)
  let case_succ = λp λa λb λc (a λax λay (b λbx λby
    let cx = (Add p (Mul p ax bx) (Rot p (Mul p ay by)))
    let cy = (Add p (Mul p ay bx) (Mul p ax by))
    (c cx cy)))
  (s case_zero case_succ a b)

// mix : ∀ n m -> G (n + m) -> G (n + m) -> G (2 + n + m)
(Mix s m t a b) =
  let case_zero = λm λt λa λb λc
    let b = (t λx(Rot m x) b)
    (c (C a b) (C a (Neg m b)))
  let case_succ = λp λm λt λa λb λc (a λax λay (b λbx λby
    let p0 = (Mix p m (IO t) ax bx)
    let p1 = (Mix p m (II t) ay by)
    (c p0 p1)))
  (s case_zero case_succ m t a b)

// imix : ∀ n m -> G (n + m) -> G (n + m) -> G (n + m)
(IMix s m t a b) =
  let case_zero = λm λt λa λb λc
    let b = (t λx(IRot m x) b)
    let u = (Add m a b)
    let v = (Add m a (Neg m b))
    (u λux λuy (v λvx λvy (c ux vy)))
  let case_succ = λp λm λt λa λb λc (a λax λay (b λbx λby
    let p0 = (IMix p m (IO t) ax bx)
    let p1 = (IMix p m (II t) ay by)
    (c p0 p1)))
  (s case_zero case_succ m t a b)

// fft : ∀ n m -> G (n + m) -> G (2n + m)
(FFT s m a) =
  let case_zero = λa λm a
  let case_succ = λp λa λm (a λax λay
    let p0 = (FFT p m ax)
    let p1 = (FFT p m ay)
    (Mix p ((A m) p) IZ p0 p1))
  (s case_zero case_succ a m)

// ifft : ∀ n m -> G (n + m) -> G m
(IFFT s m a) =
  let case_zero = λa λm a
  let case_succ = λp λa λm (a λax λay
    let sm = (S m)
    let p0 = (IFFT p sm ax)
    let p1 = (IFFT p sm ay)
    (IMix p sm IZ p0 p1))
  (s case_zero case_succ a m)

(Show s a) =
  let case_zero = λa (a (- 0.0 1.0) 0.0 1.0)
  let case_succ = λp λa (a λaxλay[(Show p ax) (Show p ay)])
  (s case_zero case_succ a)

Main =
  let s = 5
  let x = (All (N s))
  let x = (FFT  (N s) (N 0) x)
  let x = (IFFT (N s) (N 0) x)
  (Show (N s) x)
```
