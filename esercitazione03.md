## Find-S

```
START
1. h = <x x>
2. esempio 1 <0 0> -> h = <0 0>
3. return h
END

h = <0 0> = *piccola* && *chiara*
In base all'ipotesi trovata, Maria non comprerebbe una borsetta grande scura.
```




## Candidate eleimination

```
START
G = { <? ?> }
S = { <x x> }

Esempio 1: <0 0> positivo
    G = { <? ?> }
    S = { <0 0> }
Esempio 2: <0 1> negativo
    G = { <? 0> }
    S = { <0 0> }
Esempio 3: <1 0> negativo
    G = { <0 0> }
    S = { <0 0> }
RETURN:
    G = { <0 0> }
    S = { <0 0> }
END

G==S quindi l'unica ipotesi contenuta nel
version-space e' *piccola* && *chiara*
In base all'ipotesi trovata, Maria non comprerebbe una borsetta grande scura.
```




## ID3

```
X     = { (<0 0>, 1); (<0 1>, 0); (<1 0>, 0) }
T     = A Maria piace
Attrs = { Col, Dim }

ID3( X, T, Attrs )
    0. DT = ( root )
    5. Entropy(S) = 1/3·log2(3) + 2/3·log2(3/2) = 0.918
       Gain(S,Col) = 0.918 - ( (2/3)·1 + (1/3)·0 ) = 0.251 -> BEST
       Gain(S,Dim) = 0.918 - ( (2/3)·1 + (1/3)·0 ) = 0.251
       A = Col
       DT = ( Col )
    6. Vi = 0 :
    7.     DT = ( (sx) 0<- Col )
    8.     Xi = { (<0 0>, 1); (<0 1>, 0) }
   10.     sx = ID3(Xi, T, { Dim })
                0. DT = ( root )
                5. Entropy(S) = 1/2·log2(2) + 1/2·log2(2) = 1
                   Gain(S,Dim) = 1 - ( (1/2)·0 + (1/2)·0 ) = 1 -> BEST
                   A = Dim
                   DT = ( Dim )
                6. Vi = 0 :
                7.     DT = ( (sx) 0<- Dim )
                8.     Xi = { (<0 0>, 1) }
               10.     sx = ID3(Xi, T, { })
                           0. DT = ( root )
                           1. DT = ( True )
                              return DT
                       DT = ( ( True ) 0<- ( Dim ) )
                6. Vi = 1 :
                7.     DT = ( ( True ) 0<- ( Dim ) ->1 (dx) )
                8.     Xi = { (<0 1>, 0) }
               10.     dx = ID3(Xi, T, { })
                           0. DT = ( root )
                           1. DT = ( False )
                              return DT
                       DT = ( ( True ) 0<- ( Dim ) ->1 ( False ) )
               11. return DT
           DT = ( ( ( True ) 0<- ( Dim ) ->1 ( False ) ) 0<- Col )
    6. Vi = 1 :
    7.     DT = ( ( ( True ) 0<- ( Dim ) ->1 ( False ) ) 0<- Col ->1 (dx) )
    8.     Xi = { (<1 0>, 0) }
   10.     dx = ID3(Xi, T, { Dim })
                0. DT = ( root )
                1. DT = ( False )
                   return DT
           DT = ( ( ( True ) 0<- ( Dim ) ->1 ( False ) ) 0<- Col ->1 ( False ) )
   11. return DT


E quindi si ottiene il seguente albero di decisione:

                       (Col)
                       /   \
                      0     1
                     /       \
                  (Dim)    (False)
                   / \
                  0   1
                 /     \
             (True)   (False)

In base all'ipotesi trovata, Maria non comprerebbe una borsetta grande scura.
```
