### Queue
- FIFO structure (First-In-First-Out)
- means an element which is inserted first will be the first element to be removed from the queue.
- elements are added from one end and elements are deleted from another end. 
- but, exception being the Priority Queue in which elements are removed from one end, 
    - but elements are added according to the order defined by the supplied comparator
- we can’t add or get or set elements at an arbitrary position in the queues.

### Properties
- Null elements are not allowed in the queue. 
    - If we try to insert null object into the queue, it throws NullPointerException.
- can have duplicate elements
- queue is not random access. i.e you can’t set or insert or get elements at an arbitrary positions.
- there are two methods to obtain and remove the elements from the head of the queue. 
    - they are poll() and remove(). 
    - the difference between them is:
        - poll() returns null if the queue is empty
        - remove() throws an exception if the queue is empty.
- two methods in the Queue interface to obtain the elements but don’t remove.
    - peek() returns null if the queue is empty
    - element() throws an exception if the queue is empty.

| Operation | Throws An Exception If operation is not possible | Returns null or false if operation is not possible |
|---|---|---|
| Add an element to the queue. |  boolean add(E e) |  boolean offer(E e) |
| Retrieve an element from the head of the queue. |  E element() | E peek() |
| Retrieve And Remove an element from the head of the queue. | E remove() | E poll() |


