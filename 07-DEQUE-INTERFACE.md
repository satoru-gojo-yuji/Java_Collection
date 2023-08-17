### Deque
- Deque is a linear collection of objects which supports insertion and removal of elements from both the ends. 
- defines the methods needed to insert, retrieve and remove the elements from both the ends.
- can use it as both Queue (FIFO) as well as Stack (LIFO). 
- can't get or set or insert elements in the middle of the Deque.

| Operation |  | Throws an exception if operation fails. | Returns null or false if operation fails. |
|---|---|---|---|
| Insertion | Front End | addFirst() | offerFirst() |
|  | Rear End | addLast() | offerLast() |
| Retrieval | Front End | getFirst() | peekFirst() |
|  | Rear End | getLast() | peekLast() |
| Retrieval And Removal | Front End | removeFirst() | pollFirst() |
|  | Rear End | removeLast() | pollLast() |

### Deque As Stack :

- Deque interface has two more methods – pop() and push().
- These two methods make Deque to function as a stack (Last-In-First-Out). 

| Stack Methods | Equivalent Deque Methods |
|---|---|
| push() | addFirst() |
| pop() | removeFirst() |
| peek() | peekFirst() |

### Properties Of Deque :

- Deque can have null elements. 
- Deque can have duplicate elements.
- can’t set or get or insert the elements at an arbitrary position of Deque. i.e Random access is not possible with the Deque.
- can use removeFirstOccurrenec(E e), removeLastOccurrence(E e) and remove(E e) methods to delete the elements from the Deque.

