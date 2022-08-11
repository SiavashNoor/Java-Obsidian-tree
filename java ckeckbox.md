```java

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyFrame extends JFrame implements ActionListener {

    JButton submitButton;

    JCheckBox checkBox;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setLayout(new FlowLayout());

        this.setPreferredSize(new Dimension(400, 400));

        submitButton = new JButton();

        submitButton.setText("submit");

        submitButton.addActionListener(this);

        checkBox = new JCheckBox();

        checkBox.setText("im not a robot ");

        checkBox.setFocusable(false);  

        checkBox.setFont(new Font(null, Font.BOLD, 18));

        //checkBox.setIcon("image.png");  //           this method sets a chosen icon instead of square checkbox

        // checkBox.setSelectedIcon("image2.png");//    and when the checkBox is selected then this Icon will be shown.

        this.add(submitButton);

        this.add(checkBox);

        this.pack();

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == submitButton) {

            System.out.println(checkBox.isSelected()); //returns true or false

        }

    }

}
```