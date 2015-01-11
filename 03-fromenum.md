## Exercise 03

`toUpper` converts a lower case `Char` to an upper case one. Fix type errors.

```Haskell
fromEnum :: Char -> Int
toEnum :: Int -> Char

offset :: Int
offset = fromEnum 'A' - fromEnum 'a'

toUpper :: Char -> Char
toUpper ch = toEnum (fromEnum ch + offset)
```
