## Java Mouse listener


```java
package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.MouseEvent;

import java.awt.event.MouseListener;

public class MyFrame extends JFrame implements MouseListener {

    JLabel label;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(500, 500);

        this.addMouseListener(this);  // now this frame would respond to mouse events 

        this.setLayout(null);

        this.getContentPane().setBackground(Color.BLACK);

        label = new JLabel();

        label.setBounds(200, 200, 64, 64);

        label.setBackground(Color.LIGHT_GRAY);

        label.setOpaque(true);

        label.addMouseListener(this); // add mouse listener to the label .

        this.add(label);

        this.setVisible(true);

    }

    @Override

    public void mouseClicked(MouseEvent e) {

        // Invoked when a mouse button has been clicked (pressed and released )on a component .

        if (e.getSource() == label) {

            System.out.println("mouse clicked ");

        }

    }

    @Override

    public void mousePressed(MouseEvent e) {

        //invoked when a mouse button has been pressed on a component.

        if (e.getSource() == label) {

            System.out.println("mouse is  pressed:");

        }

    }

    @Override

    public void mouseReleased(MouseEvent e) {

        //invoked when a mouse button has been released on a component .

        if (e.getSource() == label) {

            System.out.println("mouse is released ");

        }

    }

    @Override

    public void mouseEntered(MouseEvent e) {

        //invokes when  the mouse enters the area of component .

        if (e.getSource() == label) {

            System.out.println("mouse entered the label");

            label.setBackground(new Color(0x6caec7));

        }

    }

    @Override

    public void mouseExited(MouseEvent e) {

        //invokes when the mouse gets out of component area.

        if (e.getSource() == label) {

            System.out.println("mouse has got out of label");

            label.setBackground(Color.LIGHT_GRAY);

        }

    }

}
```

.