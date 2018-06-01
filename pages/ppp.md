---
layout: pages
title: PPP
description: PPP
---

### PPP

Most people connect to the Internet through some kind of dialup connection. The common one is PPP, though SLIP is still occasionally used. Setting up your system to speak PPP to a remote server is pretty easy. We've included a few tools to help you in setting it up.

**pppsetup**

In Slackware we have included a program called pppsetup to configure your system to use your dialup account. It shares a look and feel similar to our netconfig program.

To run the program, make sure you are logged in as root. Then type pppsetup to run it. You should see a screen like this:

![Screenshot of pppsetup](/assets/images/pppsetup.gif){: class="img-fluid"}

The program will present a series of questions, to which you will feed it appropriate answers. Things like your modem device, the modem initialization string, and the ISP phone number. Some items will have a default, which you can accept in most cases.

After the program runs, it will create a ppp-go program and a ppp-off program. These are used to start and stop, respectively, the PPP connection. The two programs are located in /usr/sbin and need root priviledges to run.

**/etc/ppp**

For most users, running pppsetup will be sufficient. However, there may be an instance where you want to tweak some of the values used by the PPP daemon.

All of the configuration information is kept in /etc/ppp. Here is a list of what the different files are for:

**ip-down**	This script is run by pppd after the PPP connection is ended.

**ip-up**	This script is run by pppd when there's a successful ppp connection. Put any commands you want run after a successful connection in this file.

**options**	General configuration options for pppd.

**options.demand**	General configuration options for pppd when run in demand dialing mode.

**pppscript**	The commands sent to the modem.

**pppsetup.txt**	A log of what you entered when you ran pppsetup.

**NOTE:** Most of these files won't be there until after you run pppsetup.