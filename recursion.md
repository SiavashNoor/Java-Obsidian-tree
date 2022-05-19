## Java Recursion

Recursion is the technique of making a function call itself.


``` java

public class Main {
  public static void main(String[] args) {
    int result = sum(10);
    System.out.println(result);
  

 public static int sum(int k) {
    if (k > 0) {
      return k + sum(k - 1);
    } else {
      return 0;
    }}}
```

## Halting Condition
Every recursive function should have a halting condition, which is the condition where the function stops calling itself. In the previous example, the halting condition is when the parameter `k` becomes 0.
`


The developer should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power. However, when written correctly recursion can be a very efficient and mathematically-elegant approach to programming.

