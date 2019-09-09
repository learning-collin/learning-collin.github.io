---
layout: default
title: Operating Systems
parent: Fundamentals
nav_order: 1
permalink: /curriculum/fundamentals/os
---

# Operating Systems
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Operating Systems

# Manjaro Linux

## Background 

[Why should you learn to use linux?]

A linux distribution_ _('distro') is an operating system
based on the [linux kernel](https://en.wikipedia.org/wiki/Linux\_kernel). Linux
distros comprise a linux kernel, a window system, a window manager, and a
desktop environment. We will install Manjaro Linux, a distro based on 
[Arch Linux](https://www.google.com/search?client=firefox-b-1-d&q=arch+linux).
Manjaro, like Arch, is built on a rolling release update model: rather than a
single large system update, releases are implemented using small, frequent
updates, only updating a piece of software that has been changed since the last
update. Manjaro follows arch development with an additional layer of testing:

    |  Manjaro  |  ⟶   |  Manjaro  |
    | (testing) |      |  (stable) |
         ↑                  ↑
        |                  
    |  Manjaro  |   ⟶-     ⤴
    |(unstable) |
         ↑
        
    |    Arch   |
    |           |

We will use Manjaro because we are Arch fans, but Manjaro's \~6-week release delay behind 
Arch makes it more stable, secure, and easy to install.
We will install Manjaro with the _KDE Plasma_ desktop environment, which uses
the [X Window System](https://en.wikipedia.org/wiki/X\_Window\_System) for a
GUI ("graphical user interface") environment and the Dolphin file manager.

## Set up a bootable USB

If you've been provided with a bootable USB, skip to the 'Installation' section.

#### Option 1: with `dd`
1) [Download](https://manjaro.org/download/kde/) Manjaro (KDE Plasma). The .iso
file will take a while to download.
2) Plug a USB drive into your computer.
3) In a terminal, run `lsblk` to see which 


#### Option 2: with Etcher
Etcher is a tool that allows you to flash OS images (.iso files) to SD cards
and USB drives. It provides protection for corrupted cards and helps prevent
you from wiping your entire hard drive!
1) [Download](https://www.balena.io/etcher/) the app for your OS.

See the [Arch
wiki](https://wiki.archlinux.org/index.php/USB_flash_installation_media#Using_etcher)


## Installation
1) If your computer is powered on, power it off. Insert the bootable thumb
drive and turn your computer on. While it is powering on, press and hold the
\<Option\> key (Mac) or repeatedly press the \<F12\> key (Windows) to open the
boot loader.

(The [boot loader](https://en.wikipedia.org/wiki/Booting#Modern_boot_loaders) is
a small program in the computer's read-only memory (ROM) that loads the
operating system to the computer's random-access memory (RAM).)

2) The boot loader will display several rows of text, indicating the hardware
from which to boot. Use the arrow keys to scroll down to one that includes
"USB" or "CD/DVD ROM". (If one doesn't work, reboot, repeat the steps above,
and try the other.)

Manjaro will load to ROM and a "Welcome to Manjaro" screen will appear. Use the
arrow keys to scroll to the "Boot: Manjaro.x86_64 kde" row and press \<Enter\>.
Wait while Manjaro boots; a console log of all the processing being starting
will display while the OS is booting.

3) You are now on Manjaro! A "Welcome to Manjaro!" window will open
automatically. To begin installing it on your computer (remember, it has been
loaded to ROM from the USB, not from your computer's hard drive), click the
"Launch installer" button.

4) If you are not plugged into a power source, the installer will give you a
warning. I advise plugging your computer in. You will see another warning about
not being connected to the internet. Click the Wifi symbol near the
bottom-right of the status bar and enter your Wifi information.

5) Click "Next", and in the next two dialogs select your time zone information
and preferred keyboard layout.

6) On the next screen you will be presented with four options:
    - Install alongside: this will keep your current OS, but install Manjaro
      alongside it. This will allow you to boot into Manjaro _or_ your current
      OS (but not both at the same time!).
    - Replace a partition: if your hard drive is already partitioned, you can
      choose which partition on which to install Manjaro
    - Erase disk: this will delete your current OS and replace it with Manjaro
    - Manual partitioning: if you know what you're doing, choose this option

If you're unsure of what to select, choose 'Install alongside'. Follow the
prompts to resize the partitions (default is 50/50) and then click "Next".

7) Enter your name (this is just for the login screen).

In the "What name do you want to use to log in?" box, enter a username. I like
to keep this simple (I always use "g"), if only because it takes up space in
the console (more on this later).

In the "What is the name of this computer?" box, choose a name for your
computer. This can be whatever you want, but I like to keep it short for the
same reason as above (names I have used include "freddie" and "eliot").

Choose a password. Do not use the same password as your online accounts. You'll
have to type this password a LOT, so I really recommend something easy to type.

Click the "Use the same password for the administrator account." box; this
computer is for personal use, so you are the administrator. Click "Next",
review the changes, and install!

## Configuration


## Wrap-up

There is a wealth of information about customization, configuration, and
troubleshooting at the [Manjaro
wiki](https://wiki.manjaro.org/index.php?title=Main_Page#Getting_Started).
