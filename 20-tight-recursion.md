# Exercise 20

```Haskell
prim c f 0 = c
prim c f n = f n (prim c f (n - 1))
```
The `prim` function passes `c` and `f` over and over despite they are loop invariants. 
Rewrite `prim` to use an inner function so they are kept in a closure instead.
