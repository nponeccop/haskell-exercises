# Exercise 24

```Haskell
data Empty = Empty | Node EmptyTree EmptyTree
allPossibleTrees = Empty : [Node x y | x <- allPossibleTrees, y <- allPossibleTrees]
```

The code attempts to generate an infinite list of all possible trees, sorted by number of nodes. The code
seems to work, but there is a counterexample: there should be 42 trees with 5 nodes. Fix the code and write 
a test to ensure that the above property holds.
