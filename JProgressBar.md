JProgressBar


```java
package package1;

//  progress bar = visual aid to  let the user know that an operation is proceeding .

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyFrame implements ActionListener {

    JFrame frame = new JFrame();

    JProgressBar bar = new JProgressBar();

    JButton button;

    MyFrame() {

        bar.setValue(0);  //a method to set progress  bar value .

        bar.setBounds(0, 0, 420, 50);

        bar.setStringPainted(true); // makes the percent value visible on progress bar .

        button = new JButton("done");

        button.setVisible(false);

        button.setBounds(170, 100, 80, 40);

        button.setFocusable(false);

        button.setBackground(Color.GRAY);

        button.setForeground(Color.WHITE);

        button.setFont(new Font(null, Font.BOLD, 17));

        button.addActionListener(this);

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setSize(500, 500);

        frame.setLayout(null);

        frame.setVisible(true);

        frame.add(bar);

        frame.add(button);

        //simulation method

        fill();

    }

    // A progress bar simulation

    public void fill() {

        int counter = 0;

        while (counter < 100) {

            counter++;

            bar.setValue(counter);

            try {

                Thread.sleep(50);

            } catch (InterruptedException e) {

                e.printStackTrace();

            }

        }

        bar.setString("done!");  //after the bar is completed this message will be shown.

        button.setVisible(true);  //shows the "done" button

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == button) {

            //System.exit(0);   // this closes the whole application.

            frame.setVisible(false);  // this hides the frame;

        }

    }

}
```