# Exercise 16

The following function doesn't compile. Fix the type error.

```Haskell
tower :: Float -> Int -> Float
tower x 0 = 1
tower x n = x^(tower x (n-1))
```
