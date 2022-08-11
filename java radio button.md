
RadioButton  = one or more buttons in a grouping in which only 1 may be selected per grou
```java 


package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

//JRadioButton  = one or more buttons in a grouping in which only 1 may be selected per group

public class MyFrame extends JFrame implements ActionListener {

    JButton submitbutton;

    JRadioButton button1;

    JRadioButton button2;

    JRadioButton button3;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setLayout(new FlowLayout());

        this.setPreferredSize(new Dimension(400, 400));

        this.getContentPane().setBackground(Color.yellow); //set frame background color .

        submitbutton = new JButton();

        submitbutton.setText("submit");

        submitbutton.setBackground(Color.blue);

        submitbutton.setFocusable(false);

        submitbutton.setForeground(Color.black);

        submitbutton.addActionListener(this);

        button1 = new JRadioButton("pizza");

        button1.addActionListener(this);

        button2 = new JRadioButton("hamburger");

        button2.addActionListener(this);

        button3 = new JRadioButton("hotdog");

        button3.addActionListener(this);

        ButtonGroup group = new ButtonGroup(); // lets just  one button of all to be selected .

        group.add(button1);   //should add buttons to the group.

        group.add(button2);

        group.add(button3);

        this.add(submitbutton);

        this.add(button1);

        this.add(button2);

        this.add(button3);

        this.pack();

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == submitbutton) {

            System.out.println(button1.isSelected() + " " + button2.isSelected() + " " + button3.isSelected());

        }

        //the Radio button is actually an event trigger. so we can use it with out implementing a seperate button .

        if (e.getSource() == button1) {

            System.out.println("you have ordered pizza ");

        }

        if (e.getSource() == button2) {

            System.out.println("you have ordered hamburger");

        }

        if (e.getSource() == button3) {

            System.out.println("you have ordered hotdog");

        }

    }

}
```