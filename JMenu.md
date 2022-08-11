JMenu in Java

The JMenuBar class is used to display menubar on the window or frame. It may have several menus. **The object of JMenu class is a pull down menu component which is displayed from the menu bar**. It inherits the JMenuItem class. The object of JMenuItem class adds a simple labeled menu item.

```java
package package1;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

import java.awt.event.KeyEvent;

public class MyFrame extends JFrame implements ActionListener {

    JMenuItem saveItem;

    JMenuItem loadItem;

    JMenuItem exitItem;

    JMenuItem openItem;

    MyFrame() {

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.setSize(500, 500);

        this.setLayout(new FlowLayout());

        JMenuBar menuBar = new JMenuBar();

        JMenu fileMenu = new JMenu("Files"); //main menu Items appears on the menu bar.

        JMenu editMenu = new JMenu("Edit");

        JMenu helpMenu = new JMenu("Help");

        JMenu viewMenu = new JMenu("View");

        JMenu windowMenu = new JMenu("Windows");

        JMenu newMenu = new JMenu("New");

        ImageIcon exitIcon = new ImageIcon("D:\\java codes\\media\\exit-icon-4600.png");

        ImageIcon openIcon = new ImageIcon("D:\\java codes\\media\\directory-icon-png-12404.png");

        ImageIcon newIcon = new ImageIcon("D:\\java codes\\media\\plus-icon-13070.png");

        JSeparator menuSeperator = new JSeparator();  //  this is a separator line  to separate the Jmenu Items

        saveItem = new JMenuItem("Save               ");

        loadItem = new JMenuItem("Load");

        exitItem = new JMenuItem("Exit");

        openItem = new JMenuItem("Open");

        JMenuItem newProject = new JMenuItem("New Project            ");

        JMenuItem NewPage = new JMenuItem("New Page ");

        saveItem.addActionListener(this);

        loadItem.addActionListener(this);

        exitItem.addActionListener(this);

        openItem.addActionListener(this);

        exitItem.setIcon(exitIcon);  // set image Icon for Jmenu Item s

        openItem.setIcon(openIcon);

        newMenu.setIcon(newIcon);

        //the mnemonic method helps to access items by shortcut Characters .

        // accepts to type of arguments  first use enum of KeyEvent .

        //or insert the  desired character to method .

        windowMenu.setMnemonic(KeyEvent.VK_W);

        fileMenu.setMnemonic(KeyEvent.VK_F);

        saveItem.setMnemonic('S');

        loadItem.setMnemonic(KeyEvent.VK_L);

        openItem.setMnemonic(KeyEvent.VK_O);

        exitItem.setMnemonic(KeyEvent.VK_E);

        //make another submenu for "New" item .

        newMenu.add(newProject); 

        newMenu.add(NewPage);

        fileMenu.add(newMenu);

        fileMenu.add(openItem);

        fileMenu.add(loadItem);

        fileMenu.add(saveItem);

        fileMenu.add(menuSeperator);

        fileMenu.add(exitItem);

        menuBar.add(fileMenu);

        menuBar.add(editMenu);

        menuBar.add(viewMenu);

        menuBar.add(windowMenu);

        menuBar.add(helpMenu);

        this.setJMenuBar(menuBar);  

        this.setVisible(true);

    }

    @Override

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == saveItem) {

            System.out.println("you have saved the file ");

        }

        if (e.getSource() == loadItem) {

            System.out.println("you have loaded the file successfully");

        }

        if (e.getSource() == exitItem) {

            System.exit(0); // shots down the program

        }

    }

}

```