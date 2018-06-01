---
title: Why use
subtitle: "Frequently Asked Questions"
layout: pages
---

### 1. Introduction

---

I use the Slackware distribution, it's no secret to anyone and I defend my distribution with a tooth and nail. Several times I'm asked, "Why do you use Slackware?" Others have already asked if Slackware is suitable for this or that.

I think Slackware users first use It because it works, but there are several other technical reasons that make us prefer a distribution where one of the main focuses is simplicity.

### 2. Advantages

---

#### 2.1. Installation

This is one of the biggest advantages of Slackware, a simple installation with great explanatory menus. With the various custom kernels , we can install the distribution on a huge variety of i386 compatible computers.

The packages compiled for i386 also make this task easier. Not all distros can be installed on computers ranging from a 386 to an Athlon, with memories starting at 8MB and IDE and SCSI disks.

Unlike many other distributions, autodetection processes that can "lock" the machine are not applied, so you do not run the risk of stopping the installation because of an unsupported video card or a grumpy sound card. Incidentally, the detection of the network card (which works wonderfully well) can also be left for later, making it easier for those who do the installations on one machine and then move on to another.

Separating applications into self-contained series also helps a lot in the installation process, especially for beginners. In the case of experts, the installation can be extremely detailed, passing package by package with its description for the user to choose, allowing a great control of what is being installed and, without difficulties, installations smaller than 40MB (did anyone mention flash ?)

#### 2.2. Package System

Contrary to what some people say, Slackware does have a package system, with installation, removal and upgrade possibilities. The toolkit is so complete that it includes a utility for creating packages in the standard (and a small documentation in the manpage on how to create them) and another one to simply extract the package (and enable the inspection and correction of its content).

Adding to these characteristics, we have the advantage that Slackware packages are not tied to endless dependency tables, which do more harm than good, as we see in the various cases of cyclic dependencies and, in the case of automatic tools, installation and removal of unwanted packets. Who has had problems upgrading rpmlib and then seeing that rpm does not work anymore knows what I'm talking about, or who tries to remove sendmail and has to to remove squid ...

Much simpler and better from the point of view of system administration, the administrator knows exactly what he is installing, including knowing the dependencies to be satisfied (and then satisfying them). I would not trust a doctor who can not locate the kidney or liver of a patient, so why entrust my system to an administrator who does not know what installs?

Another advantage is the package database, which is all in text mode. This makes it much easier to search for installed files and packages and also to make utilities that use this base to propagate installations or to facilitate upgrades, or even to locate in which package a particular file is located. This only with common commands used in the shell , making it easier to recover a damaged system, or know which packages to repair. Have you tried repairing the base of the RPM packages? Or know which packages are installed with rpm not working?

#### 2.3. BSD-style initialization

Booting Slackware is one of the fastest and most efficient. It's much simpler to administer than SystemV startup: instead of hundreds (literally) of symbolic links to dozens of files, just a series of scripts that can be easily edited.

The main services are separated into separate scripts that can be called individually, and to determine which should and should not be started at boot, we only need to resort to a chmod .

I am very impressed by the fact that controlling more than a hundred symbolic links (which must still have an argument regarding the order in which they are started) may be simpler than editing a script or changing whether or not it should be executed.

With these characteristics, we can add without any difficulties new scripts and already with the advantage of being placed in the correct order. And, while being infinitely superior in ease and simplicity of use, it also supports the startup scripts in the SysV standard.

#### 2.4. Simplicity

Finally, one of the biggest philosophies in Slackware is KISS (Keep It Simple Stupid) , which means "Keep it simple, stupid!" And so it's a simple distribution, in which we can quickly find and modify the configuration files. While many distributions keep dozens of files under / etc / sysconfig containing the configuration of your system and your hardware, in Slackware this data is concentrated in /etc/rc.d , along with the startup scripts .

Text-mode configuration utilities make remote configuration via serial console and on machines without X installed; something that graphical utilities do not help much to do (when they do not make it impossible), particularly I find it strange when some distribution that says directed to servers requires the installation of X so that its utilities work in the correct way.

The greater simplicity also reflects greater consistency between the various packages and greater stability. In this case it is enough to use a little probability, the greater the complexity of the system involved, the greater the chance of errors and the more complex the error control scheme of the system. Because the error-control scheme must be more complex, it is more prone to errors, and we feed back a live wheel. Slackware escapes from this vicious circle through the simplest method, in an application of the famous Occam Razor (in the case of several equivalent models, one should prefer the simpler one).

### 3. Where to Use
---

#### 3.1. Servers

The first use to be thought of with a machine with all these characteristics

- Ease of administration;
- Stability e;
- High customization potential

It's on servers. Configuration utilities all in text mode work like a hand on the wheel in remote installations, the simplicity of the startup and configuration files make the machine reconfiguration quick and painless. Patching is smooth thanks to pkgtool and associated tools (the only problem is in downloading packages to be installed, but there are a number of tools created by the slacker community to further facilitate this process).

In short, many advantages for only one disadvantage (in this case, downloading the updates). Well, we know that a server was not meant to be reinstalled every five minutes (as users of other distributions tend to think it necessary), unless there is a big advantage over the already installed software , we should only make updates in cases of security breach. Being constantly installing one version over another only contributes to system instability.

#### 3.2. Raise machines with few resources

Compiled packages for i386, ease of administration without X, availability of XFree86 3.3.6 (which is lighter) and high customization capabilities make Slackware the ideal distribution for machines with poor memory, processing and disk resources.

Obviously we can not expect a 486 the same performance we see on a brand new Pentium IV, but we can expect it to work as a print, mail and gateway server with high efficiency and reliability.

Obsolete labs, with old machines and tiny HDs, can take advantage of Slackware very well and become quality graphics terminals. Some distributions think that only i586 (Pentium) or higher computers can have this use, Slackware does not.

#### 3.3. Desktop

Several different window managers, two full desktop environments and extensive hardware support. Need more? Browsers, Text Editors, Spreadsheets, Instant Messaging Software, FTP Clients, Graphic Editors, etc ...

The other distros also have these same programs, and if they say they are prepared for the desktop, Slackware is there too! I use Linux since 96 (started with Slackware 96) as a desktop and I have been able to write my articles and works for college, listen to music, read emails, surf, etc ...

#### 3.4. Learning

Being simple to use and simple to understand, Slackware is perfect for didactic purposes. You can know exactly what is installed, where are the configuration files, etc ... The dozens of bizarre files scattered in / etc / sysconfig , prepared to make configuration utilities easier to use, hinder the understanding of the details and the understanding of the system as a whole.

It is through understanding that we create true system administrators and not mere push buttons. Attention, it is not a question of disqualifying the configuration utilities (Slackware has several and its users create still others to facilitate and simplify the life of the administrator), but to use these utilities knowing what is happening.

### 4. Conclusion
---

With this article we can see the various advantages of Slackware in terms of system administration and maintenance. While some find it easy to enter into sixteen submenus to change the IP of the computer or to load the correct module of the network card; we, slackers , believe that it is easy to solve the problem with editing in the right place of the correct configuration file.

And this is Slackware, ease and simplicity. If this is what you want Slackware is for you, and you can figure out why it takes so many users to love this distribution. Any questions, criticisms or suggestions regarding this article, send an e-mail to [piterpk@terra.com.br](mailto:piterpk@terra.com.br).

**Font:** [Piter Punk's](http://piterpunk.unitednerds.org/artigos/porque.html).