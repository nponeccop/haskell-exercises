## Exercise 01

Fix the program below.

The program computes value of a complex polynomial at the given point.

Polynomial is given as a list of `((Int,Int),Int)` elements, where the pair `(Int,Int)` stands for real and imaginary unit of the quotient, and the remaining `Int` represents degree. Therefore, value of the polynomial in complex point `x` is computed as the sum of `a_i*(x^t)` where `a_i` is the `i`th quotient and `t` degree.

```Haskell
type Komp = (Int, Int)
(+%) :: Komp -> Komp -> Komp
(r1, i1) +% (r2, i2)	= (r1+r2, i1+i2)

(*%) :: Komp -> Komp -> Komp
(r1, i1) *% (r2, i2)	= (r1*r2 - i1*i2, r1*i2 + i1*r2)
 
(^%) :: Komp -> Int -> Komp
k ^% 1		= k
k ^% n		= (k ^% (n-1)) *% k

vredKompPol :: [(Komp,Int)] -> Komp -> Komp
vredKompPol ((k,s):poli) t	= k*%(t^%s) +% (vredKompPol poli t)
```

`+%`, `*%` and `^%` are nothing more but operations `+`, `*` and `^` defined over complex numbers represented by the type `Komp`.

The code loads fine in `ghci` but execution:

    Main> vredKompPol [((1,1),2),((1,1),0)] (0,0)

throws an error:

`ERROR - Control Stack Overflow`

