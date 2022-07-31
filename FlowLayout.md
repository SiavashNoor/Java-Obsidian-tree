The Java FlowLayout class is used to arrange the components in a line, one after another (in a flow). It is the default layout of the applet or panel.

```java

package package1;

import javax.swing.*;

import java.awt.*;

//Layout Manager =  Defines the natural layout for components within a container .

//3 common managers

//FlowLayout = places components in a row ,sized at their preferred size .

// if the horizontal space in the container is too small,

// the FlowLayout class uses teh next available row .

public class MyFrame extends JFrame {

    MyFrame() {

        JFrame frame = new JFrame();

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(700, 700);

        frame.setLayout(new FlowLayout(FlowLayout.CENTER,10, 10));//set layout of frame to the flow layout.

        //input arguments are for making space between components

        frame.add(new JButton("1")); // a short way to create a button

        frame.add(new JButton("2"));

        frame.add(new JButton("3"));

        frame.add(new JButton("4"));

        frame.add(new JButton("5"));

        frame.add(new JButton("6"));

        frame.add(new JButton("7"));

        frame.add(new JButton("8"));

        frame.add(new JButton("9"));

        frame.setVisible(true); //its better make the frame visible finally due to preventing some problems.

    }

}
```