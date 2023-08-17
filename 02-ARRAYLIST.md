### ArrayList
- re-sizable array.
- default initial capacity is 10.
```java 
public class ArrayList<E>
extends AbstractList<E>
implements List<E>, RandomAccess, Cloneable, Serializable
```
- not thread-safe i.e multiple threads can use same ArrayList simultaneously.

| Array | ArrayList |
|--|--|
| Static i.e fixed length| Dynamic i.e size is automatically increase or decrease|
| Can hold primitives and objects | Can hold only objects |
| Can be iterated using for loop and for-each| Uses Iterators to iterate|
| Size of array using length attribute| Size can be checked using size() method|
| Constant time performance for add and get operations | Also gives constant time performance for add and get operations, except resize|
| Don't support generics| Supports generics|
| Not type safe | Type safe|
| Multi-dimensional | Can't be multi-dimensional |
| Element are added using assignment operator | Elements are added using add() method |

### Constructors

```java
// Constructs an empty list with an initial capacity of ten.
public ArrayList(){} 

// Constructs an empty list with the specified initial capacity.
public ArrayList(int initialCapacity){}

// Constructs a list containing the elements of the specified collection, 
// in the order they are returned by the collection's iterator.
// Upper Bounded Wildcards: <? extends E > i.e E or subtypes of E 
public ArrayList(Collection<? extends E> c){} 

```
- ensureCapacity()
    - to manually increase the current capacity.
    - example:  list.ensureCapacity(20);
- trimToSize() 
    - method is used to trim the capacity of arrayList to the current size of ArrayList.
- size() 
    - method returns number of elements present in an ArrayList.
- isEmpty() 
    - method of ArrayList is used to check whether the given ArrayList is empty or not. 
    - this method returns true if an ArrayList contains no elements otherwise returns false.
- contains(Object o) 
    - method can examine whether the ArrayList contains the given element or not. 
- indexOf() 
    - method returns index of first occurrence of a specified element 
- lastIndexOf()
    - method returns index of last occurrence of a specified element in an ArrayList.
    - if element is not found, they will return -1.
- Object[] toArray() 
    - method returns an array containing all elements of the ArrayList. 
    - this method acts as a bridge between normal arrays and collection framework in java.
- E get(int index)
    - method returns an element from a specified position of an ArrayList. 
- E set(int index, E element) 
    - method replaces a particular element in an Arraylist with the given element.
- boolean add(E e) 
- void add(int index, E element) 
    - method which takes index and an element as arguments can be used to insert an element at a particular position of an ArrayList. 
- E remove(int index)
    - method which takes int type as an argument is used to remove an element from a particular position of an ArrayList.
- boolean remove(Object o) 
    - remove(Object obj) method removes the first occurrence of the specified element 'obj'. 
    - if that element doesn’t exist, ArrayList will be unchanged.
- clear() 
    - method removes all elements of an ArrayList. ArrayList will be empty after this method is executed.
- List<E> subList(int fromIndex, int toIndex) 
    - method returns a view of a portion of an ArrayList in the given range.
    - returned subList is backed by original ArrayList 
    - any changes made to subList will be reflected in original ArrayList or Vice-Versa.
- boolean addAll(Collection<? extends E> c)
    - method which takes Collection type as an argument to join two ArrayLists.
    - this method appends all elements of the passed collection to the end of the invoking collection.
- boolean addAll(int index, Collection<? extends E> c)
    - method inserts all of the elements of passed collection at a specified position of an ArrayList.

### Converting Array to ArrayList

- static <T> List<T> Arrays.asList(T... a)
    - is used to convert array to ArrayList.
```java
String[] array = new String[] {"ANDROID", "JSP", "JAVA", "STRUTS", "HADOOP", "JSF"};
         
ArrayList<String> list = new ArrayList<String>(Arrays.asList(array));       
```
- static <T> boolean Collections.addAll(Collection<? super T> c, T... elements)
```java
String[] array = new String[] {"ANDROID", "JSP", "JAVA", "STRUTS", "HADOOP", "JSF"};
         
ArrayList<String> list = new ArrayList<String>();

Collections.addAll(list, array);
```
- boolean ArrayList.addAll(Collection<? extends E> c)
```java
String[] array = new String[] {"ANDROID", "JSP", "JAVA", "STRUTS", "HADOOP", "JSF"};
ArrayList<String> list = new ArrayList<String>();
         
list.addAll(Arrays.asList(array)); 
```
- Using Streams
```java
String[] array = new String[] {"ANDROID", "JSP", "JAVA", "STRUTS", "HADOOP", "JSF"};
         
List<Object> list = Arrays.stream(array).collect(Collectors.toList());
```

### ArrayList To Array 

-  <T> T[] toArray(T[] a)
```java
ArrayList<String> list = new ArrayList<String>();
// ....
String[] array = new String[list.size()]; 
         
list.toArray(array);
```

### Program To Reverse An ArrayList
- static void Collections.reverse(List<?> list)
    - method reverses the elements of the given ArrayList in linear time 
    - i.e it has the time complexity of O(n)


### Removing duplicate element from ArrayList

- Removing Duplicate Elements From ArrayList Using HashSet
    - elements are shuffled after duplicate elements are removed.
    - they are not in the insertion order.
```java
ArrayList<String> listWithDuplicateElements = new ArrayList<String>();
// added elements...
HashSet<String> set = new HashSet<String>(listWithDuplicateElements);
ArrayList<String> listWithoutDuplicateElements = new ArrayList<String>(set);
```
- Removing Duplicate Elements From ArrayList Using LinkedHashSet
    - it doesn’t allow duplicate elements and also maintains the insertion order of elements
```java
ArrayList<String> listWithDuplicateElements = new ArrayList<String>();
// added elements...
LinkedHashSet<String> set = new LinkedHashSet<String>(listWithDuplicateElements);
ArrayList<String> listWithoutDuplicateElements = new ArrayList<String>(set);
```

### Different Ways Of Iterating An ArrayList In Java :
- Iterate a given ArrayList in 4 different ways. They are,
    - Iteration Using Normal for loop.
    - Iteration Using Iterator Object.
    - Iteration Using ListIterator Object.
    - Iteration Using Enhanced for loop.