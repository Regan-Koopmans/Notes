#AVL Trees

An  **AVL Tree** is a binary tree that maintains balance, so that its operational complexity is closer to  O(log(n)).

##Motivation

Binary search trees work in O(n), because in the worst case they behave like a linked list.

##How Are the Properties Maintained?

###Insert

We perform the usual insert for a binary search tree. If we find that three or more nodes sit in a line, do a rotate on the head of that sublist.

##Rotations

```
			LEFT ROTATE X
    [x]                        [Y]
   /   \                      /   \
 [A]  [Y] 		-->	   [x]   [C]
      /  \                  / \
    [B]  [C]              [A] [B]
```

The rotation maintains the in-order notation. It may sometimes take two rotations to achieve a balances tree.

##Worst case for AVL

Based on the fundamental properties, the worst case for an AVL tree is that every left and right node have a height difference of one. So the motif below repeats for every level.
```
	  /\
     / /\
    /\/  \

```
So the recursive folmula for height of AVL is
N<sub>h</sub> = 1 + N<sub>h-1</sub>+N<sub>n-2</sub>

**WHICH IS ALMOST FIBONACCI WTF??**

<pre>
N<sub>n</sub> > 1 + 2N<sub>n-2</sub>
	> 2N<sub>n-2
	= &theta;(2<sup>h/2</sup>)
h < 2log(n)
</pre>

And we know that fibonacci is exponential.
Height < 1.44log(n).