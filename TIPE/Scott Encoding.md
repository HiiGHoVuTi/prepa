
$$
\begin{align}
\text{type } T &:= A\, \alpha_{1} \dots \alpha_{n_{A}} \;|\; B \, \beta_{1}\,\dots \beta_{n_{B}} \;| \; \dots  \\
\Downarrow& \\
\text{type }T &:= \forall t.(\alpha_{1}\to\dots \to\alpha_{n_{A}} \to t)\to (\beta_{1}\to \dots \to \beta_{n_{B}} \to t) \to \dots → t
\end{align}
$$

^7c3f29

```haskell
data Nat = N | S Nat
 -- >
data Nat = forall t. t -> (Nat -> t) -> t
```

```haskell
data List x = Nil | Cons x (List x)
-- >
data List x = forall t. t -> (x -> List x -> List x) -> t
```

