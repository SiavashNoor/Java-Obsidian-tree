
## Java GUI frame


```java

package package1;
import javax.swing.*;
import java.awt.*;

public class JavaGuiPractice extends JFrame {

    // make an instance of this class in where we want to use

   JavaGuiPractice(){

       this.setVisible(true); //makes the frame visible
       this.setSize(599,599);  //defines the frame size
       this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  //

       //exit on close :after pushing the exit button the program stops execution.

       //DO_NOTHING_ON_CLOSE don't let the window close .

       //HIDE_ON_CLOSE :The hide-window default window close operation

       //DISPOS_ON_CLOSE :

       this.setResizable(false);  //don't let the frame be resized
       this.setTitle("Java GUI"); //title of frame
       this.getContentPane().setBackground(new Color(0x1a63b2));// set the background color of frame
       ImageIcon image  = new ImageIcon("C:\\Users\\ASUS\\Desktop\\128.png");

       this.setIconImage(image.getImage()); //setting icon image

   }

}
```



