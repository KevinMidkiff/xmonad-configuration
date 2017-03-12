# xmonad-configuration
Configuration files for my xmonad configuration.

This configuration is based off of this configuration [http://beginners-guide-to-xmonad.readthedocs.io/](http://beginners-guide-to-xmonad.readthedocs.io/).

# Installation
Execute the following command to install all of the needed components on Ubuntu:

```sh
$ sudo apt install xmonad suckless-tools xscreensaver xmobar stalonetray feh python-pip 
```

In order to use the <code>udiskie</code> utility you must install it using Python PIP. Use the following command to do the installation.

```sh
$ sudo pip install udiskie
```

# Setup
To setup this configuration simply run the following commands:

> **NOTE:** In this example the repository is cloned into <code>~/.xmonad-configuration/</code> directory.

```sh
$ ln -s ~/.xmonad-configuration/xmonad ~/.xmonad
$ ln -s ~/.xmonad-configuration/xmobarrc ~/.xmobarrc
$ ln -s ~/.xmonad-configuration/stalonetrayrc ~/.stalonetrayrc
$ ln -s ~/.xmonad-configuration/xsessionrc ~/.xsessionrc 
```

# GTK Theme
To change the GTK 2.0 or GTK 3.0 theme used for GUI applications you'll need to modify/add a configuration file for each GTK version.

## GTK 2.0
To change the GTK 2.0 theme that is used, you need to modify/create the <code>~/.gtkrc-2.0</code> file. Add the following to that file.

```sh
gtk-theme-name = "<YOUR THEME>"
```
>**NOTE:** You can also change the font and font size for GTK from this file.

## GTK 3.0
To change the GTK 3.0 theme that is used, you need to modify/add the <code>~/.config/gtk-3.0/settings.ini</code> file. Add the following to that file.

```ini
[Settings]
gtk-application-prefer-dark-theme=1
gtk-theme-name="<YOUR THEME>"
```

Once you have created this configuration file, you must add the following line to your <code>/etc/environment</code> file.

```sh
GTK_THEME="<YOUR THEME>"
```

# Java GUI Applications
By default Java based GUI applications do not enable using a tiling window manager. To enable this, simply add the following export to your <code>/etc/environment</code>:

```sh
_JAVA_AWT_WM_NONREPARENTING=1
```

# Sleep on Lid Close
**TODO:** Finish documenting section
 - http://www.linuxquestions.org/questions/slackware-14/current-how-to-suspend-when-closing-the-lid-on-the-laptop-4175586386/

# Other Helpful Links

- [Xmonad Tutorial Beginning Beginners](http://beginners-guide-to-xmonad.readthedocs.io/)
- [HowToGeek Tutorial](https://www.howtogeek.com/114728/how-to-use-xmonad-a-tiling-window-manager-for-linux/)
- [Xmonad a Guided Tour](http://xmonad.org/tour.html)
