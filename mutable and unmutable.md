A **mutable** object can be changed after it's created, and an **immutable** object can't.

In Java, everything (except for strings) is mutable by default:

There's no way to make existing objects immutable. Even if an object is declared final, its fields can still be changed

That said, if you're defining your own class, you can make its objects immutable by making all fields final and private.

```java
public class IntegerPair {
    private final int x;
    private final int y;

    IntegerPair(int x, int y) {
        this.x = x;
        this.y = y;
    }
}

IntegerPair p = new IntegerPair(5, 10);

p.x = 50;
// Compilation error: cannot assign a value to a final variable
```

Strings are immutable in Java.

Any time you change a string (e.g.: tacking on an extra character, making it lowercase, swapping two characters), you're actually creating a new and separate copy



Mutable objects are nice because you can make changes **in-place**, without allocating a new object. But be careful—whenever you make an in-place change to an object, _all_ references to that object will now reflect the change.

