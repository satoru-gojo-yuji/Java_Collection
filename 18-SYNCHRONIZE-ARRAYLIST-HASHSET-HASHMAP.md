### How To Synchronize ArrayList, HashSet And HashMap In Java?

|Type| How to Synchronize? | |
| ArrayList|Collections.synchronizedList()|public static <T> List<T> |synchronizedList(List<T> list)|
|HashSet|Collections.synchronizedSet()|public static <T> Set<T> synchronizedSet(Set<T> s)|
|HashMap|Collections.synchronizedMap()|public static <K,V> Map<K,V> synchronizedMap(Map<K,V> m)|

### To Synchronize ArrayList In Java
- while iterating over the synchronized list, you must use it in a synchronized block.
    - Failed to do so may result in non-deterministic behavior.
```java
 //Getting synchronized list   
        List<String> synchronizedList = Collections.synchronizedList(list);
        //you must use synchronized block while iterating over synchronizedList
        synchronized (synchronizedList) 
        {    Iterator<String> it = synchronizedList.iterator();    
            while (it.hasNext()) 
            {
                System.out.println(it.next());
            }
        }
```
### To Synchronize HashSet In Java
- we must use this synchronized set in a synchronized block while iterating over it.
    - If you don’t do this, it may result in non-deterministic behavior.
```java
  //Getting synchronized set 
        Set<String> synchronizedSet = Collections.synchronizedSet(set);  
        //you must use synchronized block while iterating over synchronizedSet
        synchronized (synchronizedSet) 
        {   Iterator<String> it = synchronizedSet.iterator();  
            while (it.hasNext()) 
            {
                System.out.println(it.next());
            }
        }
```
### To Synchronize HashMap In Java
- we must use this synchronized map in a synchronized block while iterating over it.
    - If you don’t do this, it may result in non-deterministic behavior.
```java
        Map<String, Integer> synchronizedMap = Collections.synchronizedMap(map);   
        Set<String> keySet = synchronizedMap.keySet();  
        System.out.println("Keys.............");  
        //While iterating over synchronizedMap, you must use synchronized block.
        synchronized (synchronizedMap) 
        {   Iterator<String> it = keySet.iterator(); 
            while (it.hasNext()) 
            {
                System.out.println(it.next());
            }
        } 
        Collection<Integer> values = synchronizedMap.values();
        System.out.println("Values.............");
         //While iterating over synchronizedMap, you must use synchronized block.
        synchronized (synchronizedMap) 
        {   Iterator<Integer> it = values.iterator();
            while (it.hasNext()) 
            {
                System.out.println(it.next());
            }
        }
```







