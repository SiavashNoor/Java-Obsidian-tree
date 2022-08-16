```java
package package1;

import javax.swing.*;

import java.awt.*;

public class MyFrame extends JFrame {

    MyPanel panel;

    MyFrame() {

        panel = new MyPanel();

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setPreferredSize(new Dimension(500,500));

        this.add(panel);

        this.pack();

        this.setVisible(true);

    }

}

###################################################################################

package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

public class MyPanel extends JPanel implements ActionListener {

    final int PANEL_WIDTH = 500;

    final int PANEL_HIGHT = 500;

    Image airPlane;

    Image backgroundImage;

    Timer timer;

    int xVelocity = 9;

    int yVelocity = 4;

    int x = 0;

    int y = 0;

    MyPanel() {

        this.setPreferredSize(new Dimension(PANEL_WIDTH, PANEL_HIGHT));

        this.setBackground(Color.black);

        airPlane = new ImageIcon("D:\\java codes\\media\\icons8-airplane-64.png").getImage();

        timer = new Timer(50, this);

        timer.start();

    }

    @Override

    public void paint(Graphics g) {

        super.paint(g); // causes the screen to be repainted .

        Graphics2D g2D = (Graphics2D) g; // cast g to g2d .

        g2D.drawImage(airPlane, x, y, null); //draws image on screen .

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (x >= (PANEL_WIDTH - airPlane.getWidth(null)) || x < 0) {

            xVelocity = xVelocity * (-1);

        }

        if (y >= (PANEL_HIGHT - airPlane.getHeight(null)) || y < 0) {

            yVelocity = yVelocity * (-1);

        }

        x = x + xVelocity;

        y = y + yVelocity;

        repaint(); //this method implicitly calls the paint method the java has recommended that

        //use this instead of calling the paint method directly .

    }

}
```


