# How to use the Command Line

## The Bash Shell
The Command Line (or Terminal) is a program which lets you use a programming
language designed for manipulating files. This programming language is called a
shell, and specifically, the one we are using is called the Bash shell, which
is the most widely used shell.

Whenever Bash displays the "prompt," this means that it is ready to receive a
command. The prompt may look different for everyone, and it is customizable,
but for me it looks like

```
[zachary:~]
```

Classically, the prompt is just a `$`. In my case, the first part of the prompt:
the `zachary`, is my user's name. The second part: the `~`, is the current directory
(or folder). The `~` (tilde) folder means the home folder. This folder contains
all the files that my User can access. On mac this would be `/Users/zachary`.
If I want to modify files outside this folder, I would need extra permissions
or administrative privileges.

From now on, if there is a `$` in front of a command, this means that the command
is a Bash command and the `$` represents your prompt. you are not supposed to 
actually include the `$` as part of the command.

## Navigating the Filesystem
To execute a command, just type out the command, and press enter. Commands in bash
tend to be very short abbreviations. The first command I'll show you is the `ls`
command, which stands for `list` or `list files`. Type this out and press enter.

It should list out all of the files in the current directory (the home directory).

Some of these files will be folders, and others will be actual files (such as
text files, word files...).

The next command is the `cd` command, which stands for `change directory`. This lets
you change the current working directory. Type

```
$ cd Desktop
```

This will change your current directory to the Desktop folder. My prompt now looks
like:

```
[zachary:~/Desktop]
```

If you run the `ls` command now, it should list all the files in your Desktop
folder.

You can get back to the home folder in 3 different ways. `..` is a special
folder name which refers to the folder above the current one. So typing
`cd ..` would take you to the folder above `Desktop`, which is the home
folder. You can also reference the home folder (`~`) from anywhere in your
system, so typing `cd ~` would also work. Lastly, `cd` is made so that if
you provide no inputs and just execute `cd` it will take you to your home
folder.

## The Structure of a Command

A Bash command is usually structure in the following way:
```
$ commandName options inputs
```

With the `cd` command, `cd` is the command name, and the folder (`Desktop` for
example) is the input. `cd` has no options.

With `ls` we have not included any options or inputs. However, 
options do exist for the `ls` command. Options (also known as flags) always
begin with a `-` or `--`. One option for `ls` is the `-l` flag. This stands for
`long`. Try running
```
$ ls -l
```
You should see that all the files will be listed in a longer format, with more
information for each file.

Another option for ls is the `-a` command, which stands for `all`. `ls` does not
show you hidden files (files that start with a `.`) by default. The `-a` command
will let you see these files.

Run
```
$ ls -a
```

This time you might see some files starting with a `.`. You should at least see
two extra files: `.` and `..`. These are special folders. The `.` folder means
the current folder. Try running `cd .`. You should see that nothing happens,
because you are changing the current directory to the current directory.
We already know what `..` means the directory above the current one.

When you execute a command, you can use multiple flags. So if you run `ls -a -l` 
you'll get all the files in long form. The `ls` command, and various others, let
you put the options together, so `ls -a -l` is equivalent to `ls -al`.
