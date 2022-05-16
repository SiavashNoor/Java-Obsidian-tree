When you know exactly how many times you want to loop through a block of code, use the `for` loop instead of a `while` loop:
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```

**Statement 1** is executed (one time) before the execution of the code block.

**Statement 2** defines the condition for executing the code block.

**Statement 3** is executed (every time) after the code block has been executed.


## Java For -Each loop 
There is also a "**for-each**" loop, which is used exclusively to loop through elements in an [**array**](https://www.w3schools.com/java/java_arrays.asp):
```java
for (type variableName : arrayName) {
  // code block to be executed
}
```

