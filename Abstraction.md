## Abstract Classes and Methods

Data **abstraction** is the process of hiding certain details and showing only essential information to the user.  
Abstraction can be achieved with either **abstract classes** or [**interfaces**](https://www.w3schools.com/java/java_interface.asp)


The `abstract` keyword is a non-access modifier, used for classes and methods:

-   **Abstract class:** is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
  
-   **Abstract method:** can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).

An abstract class can have both abstract and regular methods:

```java
abstract class Animal {
  public abstract void animalSound();
  public void sleep() {
    System.out.println("Zzz");
  }
}
```


#### Why And When To Use Abstract Classes and Methods?

To achieve security - hide certain details and only show the important details of an object.

**Note:** Abstraction can also be achieved with [Interfaces](https://www.w3schools.com/java/java_interface.asp)




