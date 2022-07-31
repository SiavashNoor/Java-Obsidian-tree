**GridLayout(int rows, int columns, int hgap, int vgap):** creates a grid layout with the given rows and columns along with given horizontal and vertical gaps.

```java

package package1;

import javax.swing.*;

import java.awt.*;

//Layout Manager =  Defines the natural layout for components within a container .

//3 common managers

//GridLayout  =  places components in a grid of cells .

// Each component takes all the  available space within its cell,

// and each cell is the same size.

public class MyFrame extends JFrame {

    MyFrame() {

        JFrame frame = new JFrame();

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(300, 300);

        frame.setLayout(new GridLayout(3, 3,10,10));//set layout of frame to the GridLayout

        //input arguments are for number of rows and columns and the last two defines the gap .

        frame.add(new JButton("1"));

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
```

