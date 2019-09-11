---
layout: default
title: Linux
parent: Fundamentals
nav_order: 2
permalink: /curriculum/fundamentals/linux
---

# Linux
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Background

## Paths
Open up a terminal window (Alt+Shift+A is the default in Manjaro). 

Linux directories are organized in a tree structure, beginning with the "root"
directory. Directory paths are delineated by the slash symbol; since root is the
bottom-level directory of the tree, it is often referred to with a bare slash symbol: "/".

To see a visualization of the root directory tree, type `tree -L 1 /` into the
terminal and press \<Enter\>. This is a bash command for visualizing file paths
as a tree; the `-L` flag limits the output to one level of directories and the
"/" indicates that we want to look at the root directory.

Most of the files you'll work with are in the `/home/$USER` directory. To see
what the tree looks like here, type `tree -L 2 /home`. Read `/home/$USER` as
"root, home, \[your username\]". Because you end up typing the path you your
home directory frequently, an "alias" (alternative name) exists for it: the
tilde ("~").

You can see which directory you are in in the terminal prompt. The prompt
consists of your username, your computer's name, and your current directory:

`[g@eliot Desktop]$`

or, if you are in your home directory:

`[g@eliot ~]$`

That dollar sign is an indicator that the terminal is awaiting input This is a
line you can enter text into; lines containing responses will not have a
prompt.

At this point, you may wonder, "Even if I know which folder I'm in, what about
where that folder is located?" To print your current filepath, use the `pwd`
("print working directory") command. Try it in the terminal now. You should see
an output that looks like:

`/home/g/Desktop`

You can also change which directory you are in with the `cd` ("choose
directory") command. `cd` takes one argument: the directory you want to move
to. Try it:

```bash
$ cd /home
$ pwd
/home
```

You can use the \<Tab\> key to autocomplete this command (and most others) as
well. Try typing "cd /" into the command line and, before hitting \<Enter\>,
pres \<Tab\> twice. All the directories inside the root directory should show
up.

```bash
$ cd /<Tab><Tab>
bin/        dev/        home/       lib64/      mnt/        proc/       run/
srv/        sys/        usr/        boot/       etc/        lib/
lost+found/ opt/        root/       sbin/       swapfile    tmp/        var/        
```

Continue by typing the letter "h" and pressing \<Tab\> again:

```bash
$ cd/h<Tab>
```

Notice that, since the `/home` directory is the only folder starting with "h",
the terminal autocompletes the command:

```bash
$ cd/home/
```

Press \<Enter\> and you will find yourself back in your home directory (check
to make sure with `pwd`!).

Another way to get back to your home directory is to type `cd ~`. An even
easier alias is simply `cd`, with no extra arguments, which does the same
thing.

We'll learn more about paths while we discuss the bash language:

## Bash Quickstart
Bash is a Unix command language, used as the default login shell
(or command-line interpreter) for most Linux distros. Bash processes commands
in a text window and can also execute commands from a file (a 'shell script'). 
Although you may never need to be a bash wizard, having a working relationship
with the language is a prerequisite to becoming an effective developer. Bash is
not necessarily a replacement for GUI tools, but in many cases it is much more
useful (indeed, it can be the only available tool) for a given application.

Bash is a scripting language in its own right, but the term "bash" is often
used interchangeably to refer to command-line tools and to the language itself.
The key point is that both bash and command-line tools are interpreted by the
terminal.

The linux command line can seem complex and scary at first. Trust me that it
will quickly seem intuitive and simple; once you grasp some basic concepts, you
will be able to use the shell effectively and continue learning on your own.

Another important command is ls, or "list". This will display the files in
your current directory. Try it now:

```bash
$ ls
Desktop  Downloads  Pictures   Documents
```

Most commands in bash can take "flags", which will change their output. `ls`,
for example, can take the -a flag, which will show hidden files, or the -l
flag, which will show ownership, permissions, and the modification date of
files (more on this later). For example:

```bash
$ ls -l
drwxr-xr-x  25 g g  4096 Sep  9 10:52  Desktop
drwxr-xr-x  11 g g  4096 Jul 18 11:49  Documents
drwx------   3 g g  4096 Sep 10 12:15  Downloads

$ ls -a
.  ..  .bash_aliases  .bash_history  .bash_profile  .bashrc  Desktop  Documents
Downloads  Pictures  .xinitrc
```

Whoa, where'd all those files come from? In bash, a `.` before a file indicates
that it is a "hidden" file. (If you're not seeing these files, enter `cd` into
the command line to go back to your home directory, then try `ls -a`
again.) These files are often used to store configuration
data or scripts. We can use `ls` to show only the files we're interested in;
let's see what the ".bash" files are all about.

```bash
$ ls -a .bash*
.bash_aliases  .bash_history  .bash_profile  .bashrc
```

(Note that the asterisk serves as a "wildcard" in bash; in the command above,
`ls` matched any filename beginning with the ".bash" string.)

These are the configuration files for bash itself, and are often referred to as
"dotfiles".  Each of these files is a valid [shell
script](https://en.wikipedia.org/wiki/Shell_script). The most "important" one
is your `.bashrc`. Bash runs this script every time you start a new terminal
session. Thus, it can be incredibly useful for configuring your system. We will
do this a little later in the "Text Editors" lesson. For the moment, to see
what is in that file, we can use the `cat` command. `cat` prints all the text
in a file. Type `cat .bashrc` into you terminal, press \<Enter\>, and see what
happens!

This output was pretty hard to read. How can we get a better sense of what's
going on? One useful too for the job is called `grep`. `grep` does a _lot_, but
it is basically a pattern matching tool. We can use `grep` to print only the
lines in .bashrc that contain a specific pattern, such as "example". But how
can we do this?

First, we have to take a small detour. Note that up to this point, we have
given the terminal an input and recieved an output. Where does that output go?
Well, so far, it has been printed to the terminal, and that's it. What if we
wanted to save that output somewhere? It turns out, this is pretty easy in
bash. Let's first try to `cat` the output of a file that doesn't exist (follow
along in the terminal):

```bash
$ cat foo.txt
cat: foo.txt: No such file or directory
```

Good, we know that there is no text file called "foo.txt". Next, let's save 



Here we must introduce the "pipe" operator, denoted by the `|` symbol.



All files that start with "bash" are run every time the system
starts up, or any time you open a new terminal window. Thus, you can add
configurations to any dotfile and it will work; the different files are there
so you don't get confused.





Although this lesson only briefly touches on more complex tools, it is worth
familiarizing yourself with `sed`, `grep`, `awk`, and other standard bash
tools.




## Permissions

## SSH 
