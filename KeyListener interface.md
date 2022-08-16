
To make a component get the keyboard focus, follow these steps:
1.  Make sure the component's `isFocusable` method returns `true`. This state allows the component to receive the focus. For example, you can enable keyboard focus for a `JLabel` component by calling the `setFocusable(true)` method on the label.
2.  Make sure the component requests the focus when appropriate. For custom components, implement a mouse listener that calls the `requestFocusInWindow` method when the component is clicked

```java 
package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.KeyEvent;

import java.awt.event.KeyListener;

// the Key listener listens to which key is pressed and has three abstract methods  that should be implemented .

public class MyFrame extends JFrame implements KeyListener {

    ImageIcon image;

    JLabel label;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(500, 500);

        this.addKeyListener(this);  // now this frame would respond to key events

        this.setLayout(null);

        this.getContentPane().setBackground(Color.BLACK);

        image = new ImageIcon("D:\\java codes\\media\\icons8-airplane-64.png");

        label = new JLabel();

        label.setBounds(0, 0, 64, 64);

        label.setOpaque(false);

        label.setIcon(image);

        this.add(label);

        this.setVisible(true);

    }

    @Override

    public void keyTyped(KeyEvent e) {

        //keyTyped = Invoked when  a key is typed .uses KeyChar,char output.

        switch (e.getKeyChar()) {

            case 'w':

                label.setLocation(label.getX(), label.getY() - 10);

                break;

            case 'a':

                label.setLocation(label.getX() - 10, label.getY());

                break;

            case 'd':

                label.setLocation(label.getX() + 10, label.getY());

                break;

            case 's':

                label.setLocation(label.getX(), label.getY() + 10);

                break;

        }

    }

    @Override

    public void keyPressed(KeyEvent e) {

        // keyPressed =  invoked  when a physical key is pressed down .uses KeyCode, int output

        //KeyCod is not Case sensitive .

        switch (e.getKeyCode()) {

            //control the image by arrow keys .

            // for arrow keys the KeyChar method wont return true value but the KeyCode method will return a value

            case 38:

                label.setLocation(label.getX(), label.getY() - 10);

                break;

            case 37:

                label.setLocation(label.getX() - 10, label.getY());

                break;

            case 39:

                label.setLocation(label.getX() + 10, label.getY());

                break;

            case 40:

                label.setLocation(label.getX(), label.getY() + 10);

                break;

        }

    }

    @Override

    public void keyReleased(KeyEvent e) {

        //keyReleased =  called when a button is released .

        System.out.println(e.getKeyChar());

        System.out.println(e.getKeyCode());

    }

}
```
