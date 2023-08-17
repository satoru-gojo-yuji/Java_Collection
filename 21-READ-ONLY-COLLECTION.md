### What Is Read Only Collection In Java?
- read only collection or unmodifiable collection is a collection which can not be modified once created. 
- we will not be able to add an element or remove an element or edit an element once you make the collection read only.
    - if we try to perform these operations on read only collection, we will get java.lang.UnsupportedOperationException. 

### How To Make Collection Read Only In J\ava?
- java.util.Collections class provides some unmodifiable wrapper methods to create read only collections in java.
- These methods take the Collection type as an argument and returns read only view of the specified collection.
-  Any modification operations on the returned collection, direct or via its iterators, will result in UnsupportedOperationException.
- these unmodifiable wrapper methods do is, any query or read operations you perform on the returned collection, will actually read through the original collection.

| Unmodifiable Wrapper Methods Of Collections Class | Description |
|---|---|
| unmodifiableCollection(Collection c) | Returns read only view of the specified collection. |
| unmodifiableList(List list) | Returns read only view of the specified list. |
| unmodifiableSet(Set s) | Returns read only view of the specified set. |
| unmodifiableMap(Map m) | Returns read only view of the specified map. |
| unmodifiableNavigableMap(NavigableMap m) | Returns read only view of the specified NavigableMap. |
| unmodifiableNavigableSet(NavigableSet s) | Returns read only view of the specified NavigableSet |
| unmodifiableSortedMap(SortedMap m) | Returns read only view of the specified SortedMap. |
| unmodifiableSortedSet(SortedSet s) | Returns read only view of the specified SortedSet. |

### How To Make ArrayList Read Only In Java?
- Collections.unmodifiableList() method is used to create read only ArrayList in java.
```java
//Creating an ArrayList
List<String> originalList = new ArrayList<String>();
//Creating read only view of the originalList
List readOnlyList = Collections.unmodifiableList(originalList);
```
### How To Make HashSet Read Only In Java?
- Collections.unmodifiableSet() method is used to create read only HashSet in java. 
```java
//Creating an HashSet
Set<String> originalSet = new HashSet<String>();
//Creating read only view of the originalSet
Set<String> readOnlySet = Collections.unmodifiableSet(originalSet);        
```
### How To Make HashMap Read Only In Java?
- Collections.unmodifiableMap() method is used to create read only HashMap in java.
```java
//Creating an HashMap
Map<Integer, String> originalMap = new HashMap<Integer, String>();
//Printing originalMap
 
Map<Integer, String> readOnlyMap = Collections.unmodifiableMap(originalMap);
              
```



















