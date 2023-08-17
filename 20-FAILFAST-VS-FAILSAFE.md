### Fail Fast Vs Fail Safe Iterators In Java
- Iterators in Java give us the facility to traverse over the Collection objects.

| Fail-Fast Iterators | Fail-Safe Iterators |
|---|---|
| Fail-Fast iterators doesn’t allow modifications of a collection while iterating over it. | Fail-Safe iterators allow modifications of a collection while iterating over it. |
| These iterators throw ConcurrentModificationException if a collection is modified while iterating over it. | These iterators don’t throw any exceptions if a collection is modified while iterating over it. |
| They use original collection to traverse over the elements of the collection. | They use copy of the original collection to traverse over the elements of the collection. |
| These iterators don’t require extra memory. | These iterators require extra memory to clone the collection. |
| Ex : Iterators returned by ArrayList, Vector, HashMap. | Ex : Iterator returned by ConcurrentHashMap. |



