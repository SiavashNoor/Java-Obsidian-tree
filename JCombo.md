## JComboBox

JComboBox is **a part of Java Swing package**. JComboBox inherits JComponent class . JComboBox shows a popup menu that shows a list and the user can select a option from that specified list . JComboBox can be editable or read- only depending on the choice of the programmerJComboBox

```java

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

//JComboBox   =  A component that combines a button or editable field and a drop_down list .

public class MyFrame extends JFrame implements ActionListener {

    JComboBox combobox;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setLayout(new FlowLayout());

        this.setPreferredSize(new Dimension(400, 400));

        this.getContentPane().setBackground(Color.yellow); //set frame background color .

        String[] cities = {"london", "new york", "paris", "tehran", "east sussex"};

        combobox = new JComboBox(cities);  //just accepts reference data type as input arguments

        combobox.setBackground(Color.BLACK);

        combobox.setForeground(Color.CYAN);

        combobox.addActionListener(this);

        //combobox.setEditable(true); //cant make any changes

        //combobox.getItemCount(); // returns amount of items .

        //combobox.addItem("ankara");

        //combobox.insertItemAt("tabriz",0); //add Item to specified index.

        //combobox.setSelectedIndex(0);//default item that is shown at the beginning

        //combobox.removeItem("tabriz");

        //combobox.removeItemAt(2);  //

        this.add(combobox);

        this.pack();

        this.setVisible(true);

    }

    //combobox  itself is an event trigger .

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == combobox) {

            System.out.println(combobox.getSelectedItem()); //returns the data itself

            System.out.println(combobox.getSelectedIndex()); //returns the index

        }

    }

}
```