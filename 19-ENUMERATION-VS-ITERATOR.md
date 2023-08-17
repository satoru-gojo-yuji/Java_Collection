### Differences Between Enumeration Vs Iterator In Java

| Enumeration | Iterator |
|---|---|
| Using Enumeration, you can only traverse the collection. You can’t do any modifications to collection while traversing it. | Using Iterator, you can remove an element of the collection while traversing it. |
| Enumeration is introduced in JDK 1.0 | Iterator is introduced from JDK 1.2 |
| Enumeration is used to traverse the legacy classes like Vector, Stack and HashTable. | Iterator is used to iterate most of the classes in the collection framework like ArrayList, HashSet, HashMap, LinkedList etc. |
| Methods : hasMoreElements() and nextElement() | Methods : hasNext(), next() and remove() |
| Enumeration is fail-safe in nature. | Iterator is fail-fast in nature. |
| Enumeration is not safe and secured due to it’s fail-safe nature. | Iterator is safer and secured than Enumeration. |

[Read more](https://javaconceptoftheday.com/differences-between-enumeration-vs-iterator-in-java/)