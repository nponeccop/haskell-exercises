# Exercise 12

Below is terribly wrong code for long addition, where numbers are represented as lists of decimal digits:

```Haskell
addLnat [x] [y] = rem  (x + y) 10 : (quot (x + y) 10) : []          
addLnat (x:xs) (y:ys) =  (rem  (x + y) 10) : w + head (addLnat xs ys)
                            where w = quot (x + y) 10
```
Fix type errors in the code above. Find a counterexample for which the code gives wrong answer.
