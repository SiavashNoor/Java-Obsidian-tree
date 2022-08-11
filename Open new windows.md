```java
//the first class

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyFrame extends JFrame implements ActionListener {

    JButton button;

    MyFrame() {

        JFrame frame = new JFrame();

        button = new JButton("open new window");

        button.setBounds(100, 100, 200, 50);

        button.setFocusable(false);

        button.setBackground(new Color(0x232323));

        button.setForeground(Color.WHITE);

        button.addActionListener(this);

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(500, 500);

        frame.setLayout(null); //when we use the manual layer management for frame

        // so then for each component that this frame contains,we should use .setBounds(); method.

        frame.add(button);

        frame.setVisible(true); //its better make the frame visible finally due to preventing some problems.

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            NewWindow newWindow = new NewWindow();

        }

    }

}
```


Second class for new window

```java 

package package1;

import javax.swing.*;

import java.awt.*;

public class NewWindow {

    JFrame frame = new JFrame();

    JLabel label = new JLabel();

    NewWindow() {

        label.setBounds(100, 250, 300, 50);

        label.setText("this is new window ");

        label.setFont(new Font(null, Font.BOLD, 20));

        frame.setDefaultCloseOperation(JFrame.HIDE_ON_CLOSE);//

        frame.setSize(500, 500);

        frame.setLayout(null); //when we use the manual layer management for frame

        // so then for each component that this frame contains,we should use .setBounds(); method.

        frame.add(label);

        frame.setLocation(200, 200); //the location of window on screen .

        frame.setVisible(true);

    }

}
```
