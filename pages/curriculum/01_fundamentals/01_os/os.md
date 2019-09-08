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
See the [Arch wiki](https://wiki.archlinux.org/index.php/USB_flash_installation_media#Using_etcher)

#### Option 3: with Rufus (Windows)
See the [Arch wiki](https://wiki.archlinux.org/index.php/USB_flash_installation_media#Using_Rufus)

### Installation
Insert the bootable thumb drive
[bootable things]

Boot up your computer (now with Manjaro!). The first row shows the current
system time, and the second displays the time zone. Using the arrow keys,
scroll down to time zone row and select it with <Enter>. Select your region 

There is a wealth of information about customization, configuration, and troubleshooting at the [Manjaro wiki](https://wiki.manjaro.org/index.php?title=Main_Page#Getting_Started).

### Wrap-up
