java key binding :

```java
package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

//Key Binding = bind an Action to a KeyStroke

//              don't require you to click a component to give it focus

//              all Swing components use Key Bindings

//              increased flexability compared to KeyListeners

//              can assigning key strokes to individual Swing components

//              more difficult to utilize and set up .

// the procedure : first create an action performed in side an action subclass. this is responsible for what would happen

//                  when we press the related Keystroke .then by using  getInputMap() method and getActionMap() method we

//                  relate the keyStroke and action together

public class MyFrame {

    JFrame frame;

    JLabel label;

    UpAction upAction;    // there are two ways to declare an action .compare this line with below line .

    Action downAction;     //  DownAction is a subclass and action is the parent class. so to declare the

    //                          child class we can use the type of the parent class .

    Action leftAction;

    Action rightAction;

    Action exitAction;

    Action hideAction;

    JButton button;

    JButton button2;

    MyFrame() {

        frame = new JFrame("key binding demo");

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        frame.setPreferredSize(new Dimension(500, 500));

        frame.setLayout(null);

        button = new JButton("OK");

        button.setBounds(200, 200, 60, 20);

        button.setFocusable(true);

        button2 = new JButton("EXIT");

        button2.setBounds(300, 200, 60, 20);

        button2.setFocusable(true);

        label = new JLabel();

        label.setBounds(0, 0, 100, 100);

        label.setBackground(Color.red);

        label.setOpaque(true);

        upAction = new UpAction();

        downAction = new DownAction();

        leftAction = new LeftAction();

        rightAction = new RightAction();

        hideAction = new HideAction();

        exitAction = new ExitAction();

        //make a pair of keyStroke-actionkeymap by 'put' method  for getInputMap

        // pass WHEN_IN_FOCUSED_WINDOW  as argument to  the input method .when we pass this argument it means that it doesn't

        //need the  object to be focused to let the keyBinding work. and when  the window is focused the keybinding  works.

        label.getInputMap(JComponent.WHEN_IN_FOCUSED_WINDOW).put(KeyStroke.getKeyStroke("UP"), "upAction");

        //creat an actionmap with actionkey, -action object .

        label.getActionMap().put("upAction", upAction);

        label.getInputMap(JComponent.WHEN_IN_FOCUSED_WINDOW).put(KeyStroke.getKeyStroke("DOWN"), "downAction");

        label.getActionMap().put("downAction", downAction);

        label.getInputMap(JComponent.WHEN_IN_FOCUSED_WINDOW).put(KeyStroke.getKeyStroke("LEFT"), "leftAction");

        label.getActionMap().put("leftAction", leftAction);

        label.getInputMap(JComponent.WHEN_IN_FOCUSED_WINDOW).put(KeyStroke.getKeyStroke("RIGHT"), "aa");

        label.getActionMap().put("aa", rightAction);

        // when we dont pass the WHEN_IN_FOCUSED_WINDOW , the key binding only works when the object is focused.

        button.getInputMap().put(KeyStroke.getKeyStroke("ENTER"), "exitAction");

        button.getActionMap().put("exitAction", exitAction);

        button2.getInputMap().put(KeyStroke.getKeyStroke("ENTER"),"hideAction" );

        button2.getActionMap().put("hideAction",hideAction);

        frame.add(label);

        frame.add(button);

        frame.add(button2);

        frame.pack();

        //makes the button focused when the window starts up .

        button.requestFocusInWindow();

        frame.setVisible(true);

    }

    //make subclasses to define the actions should be performed when we use the keyBinding .

    public class UpAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            //to define a new location for label .use the setLocation() method

            label.setLocation(label.getX(), label.getY() - 10);

        }

    }

    public class DownAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            label.setLocation(label.getX(), label.getY() + 10);

        }

    }

    public class LeftAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            label.setLocation(label.getX() - 10, label.getY());

        }

    }

    public class RightAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            label.setLocation(label.getX() + 10, label.getY());

        }

    }

    public class ExitAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            frame.setVisible(false);

        }

    }

    public class HideAction extends AbstractAction {

        @Override

        public void actionPerformed(ActionEvent e) {

            System.exit(0);

        }

    }

}

```

