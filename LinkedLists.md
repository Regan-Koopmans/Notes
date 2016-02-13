#Linked Lists

##Skip Lists

Other lists are not always appropriate because:

* Searches always begin from the front/end of the list.
* They have **no random access**.

Skip Lists are ordered linked lists that enable searches in O(ln(n)). The basic premise of skip lists is that every 2nd node points 2 nodes ahead, every 4th four nodes ahead.

###### Pseudo code for search:
```java
1. Start at highest level.
2. For every level: iterate until

    i. element is found
    ii. current element is greater than target.
    iii. end of list is found.

3. if (ii)
	 Go to previous element and go level down.

4. if (iii)
	-Go down until non-null element is found.
    	if found go there
        else element was not found.
```

The number of levels is calculated by:

``log(n) + 1 ``

(where n is the number of nodes).

##Sparse Tables

These are minimal sized table data structures. Sparse tables eliminate space wastage by using **two sets of interlinking linked lists**.

##Self-Organising Lists

There are four main self-organising lists.

1. Transpose Method.
2. Ordering.
3. Move-to-front.
4. Count Method.

####Transpose.

```java
	public T access(int n)
    {
    	if (head == null)
        	return null;
    }
```

####Move-to-front.

```java
	public T access(int n)
    {
    	if (head == null)
        	return null;
    }
```

####Count Method.

```java
	public T access(int n)
    {
    	if (head == null)
        	return null;
    }
```