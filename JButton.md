## JButton
The class JButton is **an implementation of a push button**. This component has a label and generates an event when pressed. It can also have an Image.

```java
Java Button

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

//at this frame we have created a button that by click on it makes the label visible

// this button just works for ones and then  is disabled   all is done in actionPerformed method .

public class MyFrame extends JFrame implements ActionListener {

////////////////////////////defined globally\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

    ImageIcon image = new ImageIcon("C:\\Users\\ASUS\\Desktop\\128.png");

    ImageIcon image2 =  new ImageIcon("D:\\java codes\\imageIcon.png");

    // make an instance of this class in where we want to use

    JButton button;

    //declare an instant of the image Label to use in frame.

    JLabel label;

///////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

    //frame constructor

    MyFrame() {

        button = new JButton();

        button.setBounds(100, 100, 190, 90);

        button.addActionListener(this); //  adds action listener to the button. should override action listener abstract method.

        button.setText("Print");  //set text for button.

        button.setFocusable(false);// removes the border around the text.

        button.setFont(new Font("Comic Sans ", Font.BOLD,25));

        button.setIcon(image2); // add icon image to the button

        button.setHorizontalTextPosition(JButton.RIGHT); // changes the text position relative to the image Icon .

        button.setVerticalTextPosition(JButton.CENTER);

        button.setIconTextGap(40); //make a gap between the Icon image and the text .

        button.setForeground( new Color(0x000000));// set font color

        button.setBackground(new Color(0x023324));//set background color of button.

        button.setBorder(BorderFactory.createEtchedBorder()); //change button border style .

        //define  label features .

        label  =  new JLabel();

        label.setIcon(image);

        label.setBounds(400, 80, 128, 128);

        label.setVisible(false);

        //frame features are created here .

        this.setVisible(true); //makes the frame visible

        this.setSize(599, 599);  //defines the frame size

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  //

        this.setResizable(true);  //don't let the frame be resized

        this.setTitle("Java GUI"); //title of frame

        this.getContentPane().setBackground(new Color(0x1a63b2));// set the background color of frame

        this.setLayout(null);

        this.setIconImage(image.getImage()); //setting icon image

        this.add(button);

        this.add(label);

    }

    @Override  // in this method we should override it . here we define the action  that the button should do .

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            System.out.println("click performed");

            button.setEnabled(false); // this unable the button  by putting  false in it .

            label.setVisible(true);

        }

    }

}
```

