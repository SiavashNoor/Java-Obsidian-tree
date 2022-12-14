```java 
package com.javatestSandBox;  
  
public class Student {  
    String name;  
    int age;  
    String address;  
  
    public Student(String name, int age, String address) {  
  
        this.name = name;  
        this.age = age;  
        this.address = address;  
  
    }  
  
    public void setName(String name) {  
        this.name = name;  
    }  
    public void setAge(int age ){  
        this.age =age ;  
  
    }  
    public void setAddress(String address){  
        this.address = address;  
  
    }  
}
```

the `this `  keyword reffers to the current instance of the class  that is created .

for example we have created an instance  of Student class and  call it   studentRegistery
`Student studentRegistry = new Student();`
then the 
`this.name = name;` 
means :  
`studentRegistry.name =name;`


