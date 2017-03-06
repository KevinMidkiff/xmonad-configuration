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

# Note on Using Java Based Applications
By default Java based GUI applications do not enable using a tiling window manager. To enable this, simply add the following export to your <code>~/.bashrc</code>:

```sh
export _JAVA_AWT_WM_NONREPARENTING=1
```

# Other Helpful Links

- [Xmonad Tutorial Beginning Beginners](http://beginners-guide-to-xmonad.readthedocs.io/)
- [HowToGeek Tutorial](https://www.howtogeek.com/114728/how-to-use-xmonad-a-tiling-window-manager-for-linux/)
- [Xmonad a Guided Tour](http://xmonad.org/tour.html)
