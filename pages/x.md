---
layout: pages
title: X Window System
description: X Window System
---

### Configuration X
---

Starting with Slackware-10.0, the X Window environment in Slackware is provided by Xorg. X is responsible for providing a graphical user interface. It is independent from the operating system, unlike Windows or the MacOS.

The X Window System is implemented through many programs that run in userland. The two main components are the server and the window manager. The server provides the lowlevel functions for interacting with your video hardware, thus it is system specific. The window manager sits on top of the server and provides the user interface. The advantage to this is you can have many different graphical interfaces by simply changing the window manager you use.

#### Configuring the X Server
---

Configuring X can be a complex task. The reason for this is the vast numbers of video cards available for the PC architecture, most of which use different programming interfaces. Luckily, most cards today support basic video standards known as VESA, and if your card is among them you'll be able to start X using the "startx" command right out of the box.

If this doesn't work with your card, or if you'd like to take advantage of the high-performance features of your video card such as hardware acceleration or 3-D hardware rendering, then you'll need to reconfigure X.

To configure X, you'll need to make an /etc/X11/xorg.conf file. This file contains lots of details about your video hardware, mouse, and monitor. It's a very complex configuration file, but fortunately there are several programs to help create one for you. We'll mention a few of them here.

#### xorgsetup
---

This is a simple menu driven frontend that's similar in feel to the Slackware installer. It simply tells the X server to take a look at the card, and then set up the best initial configuration file it can make based on the information it gathers. The generated /etc/X11/xorg.conf file should be a good starting point for most systems (and should work without modification).

#### xorgconfig
---

This is a text-based X configuration program that's designed for the advanced system administrator. Here's a sample walkthrough using xorgconfig. First, start the program:

`# xorgconfig`

This will present a screenful of information about xorgconfig. To continue, press enter. xorgconfig will ask you to verify you have set your PATH correctly. It should be fine, so go ahead and hit enter.

Next, select your mouse from the menu presented. If you don't see your serial mouse listed, pick the Microsoft protocol -- it's the most common and will probably work. Next xorgconfig will ask you about using ChordMiddle and Emulate3Buttons. You'll see these options described in detail on the screen. Use them if the middle button on your mouse doesn't work under X, or if your mouse only has two buttons (Emulate3Buttons lets you simulate the middle button by pressing both buttons simultaneously). Then, enter the name of your mouse device. The default choice, /dev/mouse, should work since the link was configured during Slackware setup. If you're running GPM (the Linux mouse server) in repeater mode, you can set your mouse type to /dev/gpmdata to have X get information about the mouse through gpm. In some cases (with busmice especially) this can work better, but most users shouldn't do this.

xorgconfig will ask you about enabling special key bindings. If you need this say "y". Most users can say "n" -- enter this if you're not sure.

In the next section you enter the sync range for your monitor. To start configuring your monitor, press enter. You will see a list of monitor types -- choose one of them. Be careful not to exceed the specifications of your monitor. Doing so could damage your hardware. Specify the vertical sync range for your monitor (you should find this in the manual for the monitor). xorgconfig will ask you to enter strings to identify the monitor type in the xorg.conf file. Enter anything you like on these 3 lines (including nothing at all).

Now you have the opportunity to look at the database of video card types. You'll want to do this, so say "y", and select a card from the list shown. If you don't see your exact card, try selecting one that uses the same chipset and it will probably work fine. Then choose an X server. You should have installed the server recommended for your card, but if not, you can always go back and install that later. Choose option (5) to use the X server recommended for your video card's chipset.

Next, tell xorgconfig how much RAM you have on your video card. xorgconfig will want you to enter some more descriptive text about your video card. If you like, you can enter descriptions on these three lines.

You'll be asked next about your RAMDAC and clock generator settings. You may enter them if you know the values, but the X server will probably successfully probe for these values. The next option is to run X -probeonly to find the clock settings for the card. You can try this, and if it works it will speed up X's startup time. If it fails, it's not usually a big problem. If it causes problems with your card, don't use it.

You'll then be asked which display resolutions you want to use. Again, going with the provided defaults should be fine to start with. Later on, you can edit the /etc/X11/xorg.conf file and rearrange the modes so 1024x768 (or whatever mode you like) is the default.

At this point, the xorgconfig program will ask if you'd like to save the current configuration file. Answer yes, and the X configuration file is saved, completing the setup process. You can start X now with the 'startx' command.

####  Picking a Window Manager
---

The last thing to do to setup your graphical environment is to select a window manager. There are dozens available, and we include a handful of them with Slackware. Run the xwmconfig program to set the default window manager for your system. This program will present a list of installed window managers and let you pick one.

![Configure](/assets/images/howto/setup_xwmconfig_cl.png)

Desktop environments can also be grouped into this category, as they are most closely related to a window manager. KDE and GNOME are examples of desktop environments, having a standard set of programs that look and act the same.