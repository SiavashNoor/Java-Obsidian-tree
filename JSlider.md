JSlider = a GUI component  that lets user enter a value by   using an adjustable sliding knob on a track.


```java
package package1;

import javax.swing.*;

import javax.swing.event.ChangeEvent;

import javax.swing.event.ChangeListener;

import java.awt.*;

//JSlider = a GUI component  that lets user enter a value by

//          using an adjustable sliding knob on a track.

public class MyFrame extends JFrame implements ChangeListener {

    JPanel panel;

    JLabel label;

    JSlider slider;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(420, 20);

        panel = new JPanel();

        label = new JLabel();

        label.setVisible(true);

        //label.setText(slider.getValue()+"°C");

        label.setFont(new Font(null,Font.PLAIN,15));

        label.setVerticalAlignment(JLabel.TOP);

        slider = new JSlider(0,100,50);

        slider.setPreferredSize(new Dimension(50,200));

        slider.setPaintTicks(true);  // makes minor and mojor ticks visible .

        slider.setMinorTickSpacing(10); //the distant between two minor ticks .

        slider.setMajorTickSpacing(20);

        slider.setPaintTrack(true);   //  make the track visible

        slider.setPaintLabels(true);  // add numbers to the major ticks .

        slider.setOrientation(SwingConstants.VERTICAL);  //change the orientation of slider .

        slider.setFont(new Font(null,Font.PLAIN,15));

        slider.addChangeListener(this);  // add a change listener to the slider .

        label.setText(slider.getValue()+"°C"); // set label text to get value from slider listener .

        panel.add(slider);

        panel.add(label);

        this.add(panel);

        this.pack();

        this.setVisible(true);

    }

    @Override

    public void stateChanged(ChangeEvent e) {

        label.setText(slider.getValue()+"°C");

    }

}
```