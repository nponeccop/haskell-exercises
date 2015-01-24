# Exercise 16

```Haskell
sub 5 = return [1]
sub x =
    do 
        xs <- sub (x - 1)
        return (x:xs)       

f xs = [ length (sub x) | x<-xs ]
```

`sub 10` returns `10,9,8,7,6,1` but `length (sub x)` in the comprehension apparently returns 1 instead of 6. Fix the comprehension.
