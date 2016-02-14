#Linked Lists

##Skip Lists

Other lists are not always appropriate because:

* Searches always begin from the front/end of the list.
* They have **no random access**.

Skip Lists are ordered linked lists that enable searches in O(ln(n)). The basic premise of skip lists is that every 2nd node points 2 nodes ahead, every 4th four nodes ahead.

### Pseudo code for search:
```ruby
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

###Insert
```java
	public void insert(T value)
    {
    	SkipListNode<T>[] curr = new SkipListNode[maxLevel];
        SkipListNode<T>[] prev = new SkipListNode[maxLevel];
        SkipListNode<T> newNode;
        int lvl, i;
        curr[maxLevel-1] = root[maxLevel-1];
        prev[maxLevel-1] = null;
        for (lvl = maxLevel -1; lvl >= 0; lvl--)
        {
        	while (curr[lvl] != null && curr[lvl].element.compareTo(value) < 0)
            {
            	prev[lvl] = curr[lvl];
                curr[lvl] = curr[lvl].next[lvl];
            }
            if (curr[lvl] != null && curr[lvl].element.equals(value))
            	return;
            if (lvl > 0)
            	if (prev[lvl] == null)
               {
               	curr[lvl-1] = root[lvl-1];
                   prev[lvl-1] = null;
               }
            else
            {
            	curr[lvl-1] = prev[lvl].next[lvl-1];
                prev[lvl-1] = prev[lvl];
            }
            lvl = chooseLevel();
            newNode = new SkipListNode<T>(value,lvl+1);

            //Set appropriate references.

            for (i = 0; i <= lvl; i++)
            {
            	newNode.next[i] = curr[i]
               if (prev[i] == null)
               	root[i] = newNode;
               else prev[i].next[i] = newNode;
            }
        }
    }

```

###Delete

```java
	public void delete(T value)
    {
    
    }
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
	public T access(T n)
    {
    	if (head == null)
        	return null;

		if (head.next.element.equals(n))
        {
        	Node nodePointer = head.next;
            head.next = nodePointer.next.next;
            head = nodePointer;
        }

        Node nodePointer = head;
        Node prevPointer = null;

        while (nodePointer.next != null && !nodePointer.next.element.equals(n))
        {
        	prevPointer = nodePointer;
            nodePointer = nodePointer.next;
        }
        if (nodePointer.next == null) return;

		Node temp = nodePointer.next.next;
        prevPointer.next = nodePointer.next;
        prevPointer.next.next = nodePoiner;
        nodePointer.next = temp;
        return nodePointer.element;
    }
```

####Move-to-front.

```java
	public T access(T n)
    {
    	if (head == null)
        	return null;
		if (head.element.equals(n))
        	return head.element;


    	Node nodePointer = head;
    	Node prevPointer = null;

   	 while (nodePointer != null && nullPointer.element.compareTo(n) < 0)
    	{
   	 		prevPointer = nodePointer;
   	     	nodePointer = nodePointer.next;
   	 }

        if (nodePointer == null) return null;

		prevPointer.next = prevPointer.next;
		nodePointer.next = head;
    	head = nodePointer;
        return head.element;
    }
```

####Count Method.

```java
	public T access(T n)
    {
    	if (head == null)
        	return null;
        Node nodePointer = head;
        Node prevPointer = null;
        while (nodePointer != null && !nodePointer.element.equals(n))
        {
        	prevPointer = nodePointer;
            nodePointer = nodePointer.next;
        }
        if (nodePointer == null) return;
        if (prevPointer == null)  //ie head is element.
        {
        	nodePointer.count++;
            return nodePointer.element;
        }
        else
        {
        	prevPointer.next = nodePointer.next;
            nodePointer.count++;
            Node seekNode = head;
            Node seekPrev = null;
            while ( seekNode != null && seekNode.count > nodePointer.count)
            {
            	seekPrev = seekNode;
                seekNode = seekNode.next;
            }
            if (seekNode == null) prevNode.next = nodePoiter;
            else
            {
            	Node temp = prevNode.next.next;
                prevNode.next = nodePointer;
                nodePointer.next = seekNode;
            }
           return nodePoitner.element;
        }
    }
```
---

_Regan Koopmans 2016._