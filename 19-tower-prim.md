# Exercise 19

Implement `tower` from [Exercise 17](17-tower-infinity.md) non-recursively using a scheme for primitive recursion:

```Haskell
prim c f 0 = c
prim c f n = f n (prim c f (n - 1))
```
