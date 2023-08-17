### HashMap Vs ConcurrentHashMap In Java
- The read operations on both, ConcurrentHashMap and HashMap, give same performance as read operations on both maps are not synchronized.
- Only modifying operations on ConcurrentHashMap are synchronized. Hence, add or remove operations on ConcurrentHashMap are slower than on HashMap.
- When you make HashMap synchronized externally using Collections.synchronizedMap() method, all the operations will be synchronized.
    - This will slow down the application.

| HashMap | ConcurrentHashMap |
|---|---|
| HashMap is not synchronized internally and hence it is not thread safe. | ConcurrentHashMap is internally synchronized and hence it is thread safe. |
| HashMap is the part of Java collection framework since JDK 1.2. | ConcurrentHashMap is introduced in JDK 1.5 as an alternative to HashTable. |
| HashMap allows maximum one null key and any number of null values. | ConcurrentHashMap doesn’t allow even a single null key and null value. |
| Iterators returned by HashMap are fail-fast in nature. | Iterators returned by ConcurrentHashMap are fail-safe in nature. |
| HashMap is faster. | ConcurrentHashMap is slower. |
| Most suitable for single threaded applications. | Most suitable for multi threaded applications. |
[Read more](https://javaconceptoftheday.com/hashmap-vs-concurrenthashmap-in-java/)