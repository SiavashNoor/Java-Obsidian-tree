## java swing
Hierarchy of Java Swing classes 
 

![[Pasted image 20220731100441.png]]


There are two ways to create a frame:

-   By creating the object of Frame class (association)
-   By extending Frame class (inheritance)
We can write the code of swing inside the main(), constructor or any other 
method.

### Example of Swing by Association inside constructor
```java
-   import javax.swing.*;  
-   public class Simple {  
-   JFrame f;  
-   Simple(){  
-   f=new JFrame();//creating instance of JFrame  

-   JButton b=new JButton("click");//creating instance of JButton  
-   b.setBounds(130,100,100, 40);  

-   f.add(b);//adding button in JFrame  

-   f.setSize(400,500);//400 width and 500 height  
-   f.setLayout(null);//using no layout managers  
-   f.setVisible(true);//making the frame visible  
-   }  

-   public static void main(String[] args) {  
-   new Simple();  
-   }  
-   }
- ```

### Simple example of Swing by inheritance

```java
1.  import javax.swing.*;  
2.  public class Simple2 extends JFrame{//inheriting JFrame  
3.  JFrame f;  
4.  Simple2(){  
5.  JButton b=new JButton("click");//create button  
6.  b.setBounds(130,100,100, 40);  

8.  add(b);//adding button on frame  
9.  setSize(400,500);  
10.  setLayout(null);  
11.  setVisible(true);  
12.  }  
13.  public static void main(String[] args) {  
14.  new Simple2();  
15.  }}
```





- [[JFrame]]
- [[JLabel]]
- [[JPanel]]
- [[JButton]]
- [[Open new windows]]
- [[JOptionsPane]]
- [[JTextField]]
- [[java ckeckbox]]
- [[java radio button]]
- [[JCombo]]
- [[JSlider]]
- [[JProgressBar]]
- [[JMenu]]   Menu bar in java 
- [[file chooser]]
- [[Color chooser]]
- [[KeyListener interface ]]
- [[mouseListener]]
- 