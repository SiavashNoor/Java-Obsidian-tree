## Java ArrayList

The `ArrayList` class is a resizable [array](https://www.w3schools.com/java/java_arrays.asp)

##### The difference between a built-in array and an `ArrayList` in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one) #####



```java
import java.util.ArrayList; // import the ArrayList class

ArrayList<String> cars = new ArrayList<String>(); // Create an ArrayList object
```

## Access an Item
To access an element in the `ArrayList`, use the `get()` method and refer to the index number:
```java
cars.get(0);
```


## Add Items
The `ArrayList` class has many useful methods. For example, to add elements to the `ArrayList`, use the `add()` method:
```java
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
  }
}
```


## Change an Item

To modify an element, use the `set()` method and refer to the index number:
```java
cars.set(0, "Opel");
```


## Remove an Item
To remove an element, use the `remove()` method and refer to the index number:
```java
cars.remove(0);
```


## some other methods 
`.size() `  // returns the number of elements inside the arraylist;
`.sort(); ` // sorts a list alphabetically and numerically 



## Other Types

Elements in an ArrayList are actually objects. In the examples above, we created elements (objects) of type "String". Remember that a String in Java is an object (not a primitive type). To use other types, such as int, you must specify an equivalent [wrapper class](https://www.w3schools.com/java/java_wrapper_classes.asp): `Integer`. For other primitive types, use: `Boolean` for boolean, `Character` for char, `Double` for double, etc:



