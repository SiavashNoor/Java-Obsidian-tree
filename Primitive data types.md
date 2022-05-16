# Primitive Data Types
Numeric data types
-----------------
A primitive data type specifies the size and type of variable values, and it has no additional methods.

There are eight primitive data types in Java:

Data Type 
Size

Description

`byte`

1 byte

Stores whole numbers from -128 to 127

`short`

2 bytes

Stores whole numbers from -32,768 to 32,767

`int`

4 bytes

Stores whole numbers from -2,147,483,648 to 2,147,483,647

`long`

8 bytes

Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807

`float`

4 bytes

Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits

`double`

8 bytes

Stores fractional numbers. Sufficient for storing 15 decimal digits

`boolean`

1 bit

Stores true or false values

`char`

2 bytes

Stores a single character/letter or ASCII values





Boolean data types
--------------------------------------------
A boolean data type is declared with the `boolean` keyword and can only take the values `true` or `false`

```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```




Characters 
-------------------------------------------
The `char` data type is used to store a **single** character. The character must be surrounded by single quotes, like 'A' or 'c':
```java
char myGrade = 'B';
System.out.println(myGrade);
```

Alternatively, if you are familiar with ASCII values, you can use those to display certain characters:
```java
char myVar1 = 65, myVar2 = 66, myVar3 = 67;
System.out.println(myVar1);
System.out.println(myVar2);
System.out.println(myVar3);
```






