## HashSet

HashSet class implements Set Interface. It represents the collection that uses a hash table for storage. Hashing is used to store the elements in the HashSet. It contains unique items.

```java
// Import the HashSet class
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {
    HashSet<String> cars = new HashSet<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("BMW");
    cars.add("Mazda");
    System.out.println(cars);
  }
}
```

Its better to use  the iterator to iterate in the set .
 see example below :
 ```java

 -   import java.util.*;  
-   public class TestJavaCollection7{  
-   public static void main(String args[]){  
-   //Creating HashSet and adding elements  
-   HashSet<String> set=new HashSet<String>();  
-   set.add("Ravi");  
-   set.add("Vijay");  
-   set.add("Ravi");  
-   set.add("Ajay");  
-   //Traversing elements  
-   Iterator<String> itr=set.iterator();  
-   while(itr.hasNext()){  
-   System.out.println(itr.next());  
-   }  
-   }  
-   }


```


