#Complexity Analysis

##Big-O Notation

This operation means "order of" and is used to describe the general behaviour of an algorithm.

<img src="https://camo.githubusercontent.com/07797459d6fa5146989128b194df9acc5eaca774/687474703a2f2f7777772e64617665706572726574742e636f6d2f696d616765732f61727469636c65732f323031302d31322d30372d636f6d702d7363692d3130312d6269672d6f2d6e6f746174696f6e2f54696d655f436f6d706c65786974792e706e67">

We can calculate the complexity of an algorithm by many delimeters


##Properties of Big-O

1. If f(n) = O(g(n)) and g(n) is O(h(n)) then f(n) = O(h(n)).
2. If f(n) = O(h(n))) and g(n) = O(h(n)) then f(n) + g(n) is O(h(n)).
3. an<sup>k</sup> = O(n<sup>k</sup>).
4. n<sup>k</sup> = O(n<sup>k+j</sup>) for any j > 0.
5. If f(n) = c.g(n) then f(n) = O(g(n)).
6. log<sub>a</sub>n = O(log<sub>b</sub>n) for any a,b >1
7. log<sub>a</sub>n is O(log<sub>2</sub>n) for any positive a &ne;1.