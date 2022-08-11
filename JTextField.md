```java

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyFrame extends JFrame implements ActionListener {

    JButton button;

    JTextField textField;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setLayout(new FlowLayout());

        button = new JButton("Submit");

        button.addActionListener(this);

        textField = new JTextField();

        textField.setPreferredSize(new Dimension(250, 50));

        textField.setFont(new Font(null, Font.BOLD, 20));

        textField.setForeground(new Color(0xa0f98f));

        textField.setBackground(Color.black);

        textField.setCaretColor(Color.white);  // sets the color of blinking text pointer .

        //in flowlayout the alignment is from the left .

        this.add(button);

        this.add(textField);

        this.pack();

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            System.out.println(textField.getText()); //to get the text from textfield

            textField.setText(null); // to clear the text area after pushing the submit button.

            button.setEnabled(false); //disables the button after very first click .

            textField.setEditable(false); /// makes it uneditable for client .

        }

    }
```
