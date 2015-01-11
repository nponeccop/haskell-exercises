## Exercise 11

Fix errors in the code below:

```Haskell
solve :: Int -> Integer
solve = undefined

main = do
  n <- readLn
  forM_ [1..n] (\i -> do
    m <- readLn
    printf "Case %d: %d" i (solve m))
```
