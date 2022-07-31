## JLabel
Label is a class of java Swing . JLabel is **used to display a short string or an image icon**. JLabel can display text, image or both . JLabel is only a display of text or image and it cannot get focus JLabel is inactive to input events such a mouse focus or keyboard focus.

```java
package package1;

import javax.swing.*;

import javax.swing.border.Border;

import java.awt.*;

public class Main {

    public static void main(String[] args) {

        JavaGuiPractice frame = new JavaGuiPractice();

        Border border = BorderFactory.createLineBorder(Color.green, 10);

        JLabel label = new JLabel();

        label.setText("this is label");

        label.setIcon(frame.image);  // add image icon to the JLabel

        label.setHorizontalTextPosition(JLabel.CENTER); //set text relative to the image icon

        label.setVerticalTextPosition(JLabel.CENTER);

        label.setForeground(new Color(0x000000));//sets the color of the font .

        label.setFont(new Font("Helvetica", Font.PLAIN, 30)); //set a font with size

        label.setBackground(new Color(0x809123)); // with this method we can change

        //background color of label .but to make it visible we should use the opaque method .

        label.setOpaque(true);

        label.setBorder(border); //creats a border around the frame  by creating an object of that .

        label.setVerticalAlignment(JLabel.CENTER); //this method helps to align the label img+txt

        label.setHorizontalAlignment(JLabel.CENTER);

        label.setBounds(0, 0, 200, 200); // set the position and dimension  of the label.

        frame.add(label);    //adds the label to the frame .

        frame.setLayout(null); // to manually change label alignment by label.setBounds .

    }

}
```