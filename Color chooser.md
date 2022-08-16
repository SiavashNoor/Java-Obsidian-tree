Java color chooser 

```java 

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyFrame extends JFrame implements ActionListener {

    JButton button;

    JLabel label;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(500, 500);

        this.setLayout(new FlowLayout());

        button = new JButton("Select color ");

        button.setFont(new Font(null, Font.BOLD, 14));

        button.setFocusable(false);

        button.addActionListener(this);

        label = new JLabel();

        label.setBackground(Color.white);

        label.setOpaque(true);

        label.setText("this is some text");

        label.setFont(new Font(null, Font.BOLD, 60));

        this.add(button);

        this.add(label);

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            JColorChooser colorChooser = new JColorChooser();

            //showDialog opens the color chooser dialog and you can pick a color and assign it to color object

            Color color = JColorChooser.showDialog(null, "Pick a Color", Color.BLACK);

            label.setForeground(color); // chage the color of font .

        }

    }

}
```