# AWT Program in Java

AWT stands for Abstract window toolkit is an Application programming interface (API) for creating Graphical User Interface (GUI) in Java. It allows Java programmers to develop window-based applications.

AWT provides various components like button, label, checkbox, etc. used as objects inside a [Java](https://www.javatpoint.com/java-tutorial) Program. [AWT](https://www.javatpoint.com/java-awt) components use the resources of the operating system, i.e., they are platform-dependent, which means, component's view can be changed according to the view of the operating system. The classes for AWT are provided by the Java.awt package for various AWT components.
The following image represents the hierarchy for Java AWT.
![[uo0socbk.bmp]]

**Container**

The container is a component that contains other components like button, textfield, label, etc. However, it is a subclass of the Component class.

**Panel**

The [panel](https://www.javatpoint.com/java-awt-panel) can be defined as a container that can be used to hold other components. However, it doesn't contain the title bar, menu bar, or border.
**Window**

A window can be defined as a container that doesn't contain any border or menu bar. It creates a top-level view. However, we must have a frame, dialog, or another window for creating a window.

**Frame**

The frame is a subclass of Window. It can be defined as a container with components like button, textfield, label, etc. In other words, AWT applications are mostly created using frame container.

### Java AWT Example
```java
-   import java.awt.*;  

-   public class AwtProgram1 {  
-   public AwtProgram1()  
-       {  
-   Frame f = new Frame();  
-           Button btn=new Button("Hello World");  
-           btn.setBounds(80, 80, 100, 50);  
-           f.add(btn);         //adding a new Button.  
-           f.setSize(300, 250);        //setting size.  
-           f.setTitle("JavaTPoint");  //setting title.  
-           f.setLayout(null);   //set default layout for frame.  
-           f.setVisible(true);           //set frame visibility true.  
-       }  

-   public static void main(String[] args) {  
-   // TODO Auto-generated method stub  

-           AwtProgram1 awt = new AwtProgram1();   //creating a frame.
```

### Java awt Example (extending Frame Class)
```java
1.  import java.awt.*;  
2.  public class AwtApp extends Frame {  

4.  AwtApp(){  
5.  Label firstName = new Label("First Name");  
6.  firstName.setBounds(20, 50, 80, 20);  

8.  Label lastName = new Label("Last Name");  
9.  lastName.setBounds(20, 80, 80, 20);  

11.  Label dob = new Label("Date of Birth");  
12.  dob.setBounds(20, 110, 80, 20);  

14.  TextField firstNameTF = new TextField();  
15.  firstNameTF.setBounds(120, 50, 100, 20);  

17.  TextField lastNameTF = new TextField();  
18.  lastNameTF.setBounds(120, 80, 100, 20);  

20.  TextField dobTF = new TextField();  
21.  dobTF.setBounds(120, 110, 100, 20);  

23.  Button sbmt = new Button("Submit");  
24.  sbmt.setBounds(20, 160, 100, 30);  

26.  Button reset = new Button("Reset");  
27.  reset.setBounds(120,160,100,30);  

29.  add(firstName);  
30.  add(lastName);  
31.  add(dob);  
32.  add(firstNameTF);  
33.  add(lastNameTF);  
34.  add(dobTF);  
35.  add(sbmt);  
36.  add(reset);  

38.  setSize(300,300);  
39.  setLayout(null);  
40.  setVisible(true);  
41.  }  
42.  public static void main(String[] args) {  
43.  // TODO Auto-generated method stub  
44.  AwtApp awt = new AwtApp();    
45.  }  
46.  }
```