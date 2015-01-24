# Exercise 14

Finish implementation of `createList` according to the specification.

```Haskell

createlist l1 l2 = map (f l2) l1 
    where f l x = undefined
```

```
> createlist [1,2] ['a','b','c']
[[(1,'a'),(1,'b'),(1,'c')],[(2,'a'),(2,'b'),(2,'c')]]
```

