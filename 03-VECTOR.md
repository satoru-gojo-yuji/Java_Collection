### VECTOR
```java
public class Vector<E>
    extends AbstractList<E>
    implements List<E>, RandomAccess, Cloneable, java.io.Serializable
```
- Vector class combines two features – “Re-sizable Array” and “Synchronization”
- is also dynamically grow-able and shrink-able collection
- vector class is synchronized.
- provides thread safety, only one thread can enter into a vector object at any time.
- effects the performance of an application as it makes threads to wait for object lock.
- can set the size of the Vector manually by setSize(int n)
### Capacity Increment
-  is an amount by which the capacity of the vector is automatically incremented whenever size of the vector exceeds it’s capacity
- can pass this capacity increment while creating a vector. 
- if we don't pass it will be treated as zero and capacity will be doubled 

- can traverse the vector using Enumeration object. Vector class has a method called elements() which returns an Enumeration object
```java
Enumeration<Integer> en = vector.elements();
while (en.hasMoreElements())
{    
      System.out.println(en.nextElement());  
}
```
- has separate methods to retrieve first and last element of vector object. firstElement() and lastElement().

### ArrayList VS Vector

| ArrayList | Vector |
|--|--|
| Not synchronized, not thread safe| Synchronized, thread safe|
|multiple threads can access ArrayList object simultaneously| only one thread can enter in Vector object at any moment of time during execution |
| thread need not to wait for object lock to access object| threads wait for object lock to enter into Vector object|
| better performance | lower performance because Vector is synchronized  |
| the capacity is increased by half of the current capacity |  the capacity is increased by Capacity Increment passed while creating the Vector object |
| we can't change the current size manually | we can change the size of Vector using setSize() | 
| elements can be traversed using Iterator, ListIterator and using either normal or advanced for loop |  Vector elements can be traversed using Enumeration also along with these methods |
| have to start searching for a particular element from the beginning of an Arraylist | can start searching for a particular element from a particular position in a Vector|
| it is intoduced in JDK 1.2 | Vector class is considered as Legacy code|

### Why not to use Vector class
- can achieve Thread Safety without Vector
    - can achieve thread safe ArrayList by using synchronizedList() method of Collections class. 
- Thread Safeness of Vector class is time consuming
    - each and every operation on Vector object thread safe.
    - need to acquire object lock for each operation you want to perform on vector object
    - this is the time consuming process and decreases the performance of your application
-  Enumeration Vs Iterator
    - Enumerations are faster than the Iterator
    - but it is not backed by the original collection
    - any changes made to original collection does not reflect in Enumeration object
