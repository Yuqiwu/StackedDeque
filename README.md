# StackedDeque

## Method Selections: 
We exluded almost all of the redundant methods that accomplish the same goal such as add() and addLast(). The only ones we left in were the peek() and get() methods just because some of us prefer to use get() when developing as opposed to peek().

### <b> add </b> 
<p> public boolean add(T value) 
<p> Inserts the specified element into the queue represented by this deque at the tail or last position. 

### <b> addFirst </b> 
<p> public void addFirst(T value) 
<p> Inserts the specified element at the front of this deque 

### <b> contains </b> 
<p> public boolean contains(T value)
<p> Returns true if this deque contains the specified element

### <b> iterator </b> 
<p> public Iterator<T> iterator() 
<p> Returns an iterator over the elements in this deque in proper sequence.


### <b> descendingIterator </b> 
<p> public Iterator<T> descendingIterator()
<p> Returns an iterator over the elements in this deque in reverse sequential order.


### <b> peek </b> 
<p> public T peek()
<p> Retrieves the head or first element of the deque. If the deque is empty, null is returned. 


### <b> peekLast </b> 
<p> public T peekLast()
<p>Retrieves the last element of this deque. If the deque is empty, return null. 


### <b> getFirst </b> 
<p> public T getFirst()
* Retrieves the first element of this deque.


### <b> getLast </b> 
<p> public T getLast()
* Retrieves the last element of this deque.


### <b> remove </b> 
<p> public T remove() 
* Retrieves and removes the head or the front of the queue represented by this deque. 


### <b> remove(Object) </b> 
<p> public boolean remove(Object o) 
<p> Removes the first occurrence of the specified element from this deque.


### <b> removeLast </b> 
<p> public T removeLast()
<p> Retrieves and removes the last element of this deque.


### <b> size </b> 
<p> public int size()
<p> Returns the number of elements in this deque.


### <b> isEmpty </b> 
<p> public boolean isEmpty() 
<p> Returns if the deque is empty. 
</p>


## Structure Rationale
### Our Choice: Doubly-linked node-based architecture 

We chose to use doubly-linked nodes as the underlying structure for our deque implementation for 2 primary reasons: unrestricted size and runtime. With nodes you never have to worry about size because they are linked objects which means that you can incrementally add them one by one in the front or the back. The runtime was the huge decider in our architecture descision. With an arrayList or array, adding to the front (assuming the structure is _front -> _end) is O(n) and removing from the front can be O(1) with a simple optimization. Adding and removing from the end is O(1). With a doubly linked node architecture, they are all O(1). When adding to the front you are simply making the front's previous node a new node, an O(1) operation.
