# Exercise 23

The following code constructs a function by list folding and then apples it to `Nothing`. 
Figure out what `compress` does and reimplement it without the folding trick.

```Haskell
compress xs = foldr f (const []) xs Nothing
  where
    f x r a@(Just q) | x == q = r a
    f x r _ = x : r (Just x)
```
