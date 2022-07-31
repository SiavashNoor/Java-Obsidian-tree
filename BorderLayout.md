### Java BorderLayout

The BorderLayout is used to arrange the components in five regions: north, south, east, west, and center. Each region (area) may contain one component only. It is the default layout of a frame or window. The BorderLayout provides five constants for each region:

1.  **public static final int NORTH**
2.  **public static final int SOUTH**
3.  **public static final int EAST**
4.  **public static final int WEST**
5.  **public static final int CENTER**

### Constructors of BorderLayout class:

-   **BorderLayout():** creates a border layout but with no gaps between the components.
-   **BorderLayout(int hgap, int vgap):** creates a border layout with the given horizontal and vertical gaps between the components.


```java 

package package1;

import javax.swing.*;

import java.awt.*;

//Layout Manager =  Defines the natural layout for components within a container .

//3 common managers

//BorderLayout = A BorderLayout places components in five areas :NORTH,SOUTH,EAST , WEST ,CENTER

// all extra space is placed in the center .

public class MyFrame extends JFrame {

    MyFrame() {

        JFrame frame = new JFrame();

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(700, 700);

        frame.setVisible(true);

        frame.setLayout(new BorderLayout(10, 10));//set layout of frame to the BorderLayout

        //input arguments are for making space between components

        JPanel panel1 = new JPanel();

        JPanel panel2 = new JPanel();

        JPanel panel3 = new JPanel();

        JPanel panel4 = new JPanel();

        JPanel panel5 = new JPanel();

        panel1.setBackground(Color.red);

        panel2.setBackground(Color.green);

        panel3.setBackground(Color.BLUE);

        panel4.setBackground(Color.magenta);

        panel5.setBackground(Color.ORANGE);

        panel1.setPreferredSize(new Dimension(100, 100));

        panel2.setPreferredSize(new Dimension(100, 100));

        panel3.setPreferredSize(new Dimension(100, 100));

        panel4.setPreferredSize(new Dimension(100, 100));

        panel5.setPreferredSize(new Dimension(100, 100));

        //___________________add panels to the center panel____________________\\

        panel5.setLayout(new BorderLayout(10, 10));

        JPanel panel6 = new JPanel();

        JPanel panel7 = new JPanel();

        JPanel panel8 = new JPanel();

        JPanel panel9 = new JPanel();

        JPanel panel10 = new JPanel();

        panel6.setBackground(Color.BLACK);

        panel7.setBackground(Color.pink);

        panel8.setBackground(Color.gray);

        panel9.setBackground(Color.YELLOW);

        panel10.setBackground(Color.CYAN);

        panel6.setPreferredSize(new Dimension(100, 100));

        panel7.setPreferredSize(new Dimension(100, 100));

        panel8.setPreferredSize(new Dimension(100, 100));

        panel9.setPreferredSize(new Dimension(100, 100));

        panel10.setPreferredSize(new Dimension(100, 100));

        panel5.add(panel6, BorderLayout.NORTH);

        panel5.add(panel7, BorderLayout.SOUTH);

        panel5.add(panel8, BorderLayout.WEST);

        panel5.add(panel9, BorderLayout.EAST);

        panel5.add(panel10, BorderLayout.CENTER);

        //_________________________________________________________________________\\

        frame.add(panel1, BorderLayout.NORTH);  //add panel to fame and choose its alignment .

        frame.add(panel2, BorderLayout.SOUTH);

        frame.add(panel3, BorderLayout.WEST);

        frame.add(panel4, BorderLayout.EAST);

        frame.add(panel5, BorderLayout.CENTER);

    }
```

