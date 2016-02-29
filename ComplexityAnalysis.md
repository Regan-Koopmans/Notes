#Complexity Analysis

[TOC]

##Big-O Notation

This operation means "order of" and is used to describe the general behaviour of an algorithm.

![](complexity.png)

We can calculate the complexity of an algorithm by many delimeters. One common way is to count the number of in terms your input, and the complexity will be the greatest power of 'n' in that equasion.

##Synbols of Complexity

&Omicron; - The "order of" operator, defines worst case complexity.
&Theta; - Defines the general average complexity.
&Omega; - Defines best-case complexity.

##Properties of Big-O

1. If f(n) = O(g(n)) and g(n) is O(h(n)) then f(n) = O(h(n)).
2. If f(n) = O(h(n))) and g(n) = O(h(n)) then f(n) + g(n) is O(h(n)).
3. an<sup>k</sup> = O(n<sup>k</sup>).
4. n<sup>k</sup> = O(n<sup>k+j</sup>) for any j > 0.
5. If f(n) = c.g(n) then f(n) = O(g(n)).
6. log<sub>a</sub>n = O(log<sub>b</sub>n) for any a,b >1
7. log<sub>a</sub>n is O(log<sub>2</sub>n) for any positive a &ne;1.

---

_Regan Koopmans, 2016_