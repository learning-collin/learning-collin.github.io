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

## Manjaro Linux

### Background 

A *__linux distribution__ *('distro') is an operating system
based on the (linux kernel)[https://en.wikipedia.org/wiki/Linux\_kernel]. Linux
distros comprise a linux kernel, a window system, a window manager, and a
desktop environment. We will install Manjaro Linux, a distro based on 
(Arch Linux)[https://www.google.com/search?client=firefox-b-1-d&q=arch+linux].
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
the (X Window System)[https://en.wikipedia.org/wiki/X\_Window\_System] for a
GUI ("graphical user interface") environment and the Dolphin file manager.

### Set up a bootable USB

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

See the [Arch wiki](https://wiki.archlinux.org/index.php/USB_flash_installation_media#Using_etcher)


### Installation
1) If your computer is powered on, power it off. Insert the bootable thumb
drive and turn your computer on. While it is powering on, press and hold the
\<Option\> key (Mac) or repeatedly press the \<F9\> key (Windows) to open the
boot loader.

(The [boot loader](https://en.wikipedia.org/wiki/Booting#Modern_boot_loaders) is
a small program in the computer's read-only memory (ROM) that loads the
operating system to the computer's random-access memory (RAM).)

2) The boot loader will display several rows of text, indicating the hardware from which to boot. Use the arrow keys to scroll down to one that includes "USB" or "CD/DVD ROM". 






Boot up your computer (now with Manjaro!). The first row shows the current
system time, and the second displays the time zone. Using the arrow keys,
scroll down to time zone row and select it with <Enter>. Select your region 

There is a wealth of information about customization, configuration, and troubleshooting at the [Manjaro wiki](https://wiki.manjaro.org/index.php?title=Main_Page#Getting_Started).

### Wrap-up
