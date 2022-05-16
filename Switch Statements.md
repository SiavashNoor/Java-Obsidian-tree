Use the `switch` statement to select one of many code blocks to be executed
```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

This is how it works:

-   The `switch` expression is evaluated once.
-   The value of the expression is compared with the values of each `case`.
-   If there is a match, the associated block of code is executed.
-   The `break` and `default` keywords are optional, and will be described later in this chapter




CAUTION :
if we don't use  break command in switch structure then all the acceptable and valid cases will be executed

**Break**;
When a match is found, and the job is done, it's time for a break. There is no need for more testing.

A break can save a lot of execution time because it "ignores" the execution of all the rest of the code in the switch block.

**Default**;
The `default` keyword specifies some code to run if there is no case match:
