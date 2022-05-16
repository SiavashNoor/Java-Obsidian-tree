### Arguments

The main methods get an array of strings as an argument, these are the command line arguments you may pass to your program.

Every array in java holds a variable called length that says how many elements are within that array.

We can go over the arguments with a simple for

```java
public class Arguments {
    public static void main(String[] args) {
        for (int i = 0; i < args.length; i++) {
            System.out.println(args[i]);
        }
    }
}
```

And to compile and run it with arguments:

```java
javac Arguments.java
java Arguments arg0 arg1 arg2
```