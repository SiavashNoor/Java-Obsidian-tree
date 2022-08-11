

```java
package package1;

import javax.swing.*;

// JOptionsPane = pop up a standard dailog box that prompts users for a value

//                or informs them of something

public class Main {

    public static void main(String[] args) {

        JOptionPane.showMessageDialog(null,"this is some useless info ","this is title",JOptionPane.PLAIN_MESSAGE);

        JOptionPane.showMessageDialog(null,"this is MORE useless info ","this is title",JOptionPane.INFORMATION_MESSAGE);

        JOptionPane.showMessageDialog(null,"REALLY? ","this is title",JOptionPane.QUESTION_MESSAGE);

        JOptionPane.showMessageDialog(null,"your computer has a virus  ","this is title",JOptionPane.WARNING_MESSAGE);

        JOptionPane.showMessageDialog(null,"error 403 ! call the support  ","this is title",JOptionPane.ERROR_MESSAGE);

        //this method returns an integer for whatever option that we choose .

       int i =  JOptionPane.showConfirmDialog(null,"this is massage ","this is title",JOptionPane.YES_NO_CANCEL_OPTION);

        System.out.println(i);

        // to get data from user .

        String name = JOptionPane.showInputDialog("what is your name ?");

        System.out.println("hello "+ name);

        ImageIcon image =  new ImageIcon("D:\\java codes\\imageIcon.png");

        String[] options = {"im good ","soso","really bad"};

        JOptionPane.showOptionDialog(null,"how do you fill?","this is title ",JOptionPane.YES_NO_CANCEL_OPTION,JOptionPane.INFORMATION_MESSAGE,image,options,0);

    }

}
```
