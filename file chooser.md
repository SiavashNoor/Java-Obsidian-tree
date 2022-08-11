## Java file chooser 

```java 

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

import java.io.File;

public class MyFrame extends JFrame implements ActionListener {

    JButton button;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(500, 500);

        this.setLayout(null);

        button = new JButton("Select File ");

        button.setBounds(200, 200, 120, 40);

        button.setFont(new Font(null, Font.BOLD, 14));

        button.setFocusable(false);

        button.addActionListener(this);

        this.add(button);

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            JFileChooser filechooser = new JFileChooser();

            //the current directory path  lets to set a default path for pop up window .

            filechooser.setCurrentDirectory(new File("D:\\java codes\\media"));

            /*the return state of the file chooser on popdown:

            JFileChooser.CANCEL_OPTION   ==  1

            JFileChooser.APPROVE_OPTION    == 0

            JFileChooser.ERROR_OPTION if an error occurs or the dialog is dismissed

              */

            // int response = filechooser.showOpenDialog(null); //select file to open  this method returns 0 if choose a file

            int response = filechooser.showSaveDialog(null);   //  select a file to save .

            if (response == JFileChooser.APPROVE_OPTION) {

                File file = new File(filechooser.getSelectedFile().getAbsolutePath()); // create a file object and pass in choosed file path .

                System.out.println(file);

            }

        }

    }

}
```