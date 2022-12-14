# Java Lambda Expressions

Lambda expression is a new and important feature of Java which was included in Java SE 8. It provides a clear and concise way to represent one method interface using an expression. It is very useful in collection library. It helps to iterate, filter and extract data from collection.

The Lambda expression is used to provide the implementation of an interface which has functional interface. It saves a lot of code. In case of lambda expression, we don't need to define the method again for providing the implementation. Here, we just write the implementation code.

Java lambda expression is treated as a function, so compiler does not create .class file.

## Functional Interface

Lambda expression provides implementation of _functional interface_. An interface which has only one abstract method is called functional interface. Java provides an anotation @_FunctionalInterface_, which is used to declare an interface as functional interface.
## Why use Lambda Expression

1.  To provide the implementation of Functional interface.
2.  Less coding.

## Java Lambda Expression Syntax

 (argument-list) -> {body}  

Java lambda expression is consisted of three components.

**1) Argument-list:** It can be empty or non-empty as well.

**2) Arrow-token:** It is used to link arguments-list and body of expression.

**3) Body:** It contains expressions and statements for lambda expression.



Let's see a scenario where we are not implementing Java lambda expression. Here, we are implementing an interface without using lambda expression.
## Without Lambda Expression
```java
-   interface Drawable{  
-       public void draw();  
-   }  
-   public class LambdaExpressionExample {  
-       public static void main(String[] args) {  
-           int width=10;  

-           //without lambda, Drawable implementation using anonymous class  
-           Drawable d=new Drawable(){  
-               public void draw(){System.out.println("Drawing "+width);}  
-           };  
-           d.draw();  
-       }  
-   }
```


## Java Lambda Expression Example

Now, we are going to implement the above example with the help of Java lambda expression.
```java
-   @FunctionalInterface  //It is optional  
-   interface Drawable{  
-       public void draw();  
-   }  

-   public class LambdaExpressionExample2 {  
-       public static void main(String[] args) {  
-           int width=10;  

-           //with lambda  
-           Drawable d2=()->{  
-               System.out.println("Drawing "+width);  
-           };  
-           d2.draw();  
-       }  
-   }
```

