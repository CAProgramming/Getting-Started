# Installing Xcode Command Line Tools

Installing the Xcode Command Line Tools will enable you to use programs
made for programming, such as the git version control system, the gcc
compiler, and many more tools. It's fairly straightforward, and should not
take long at all.

First, open the Terminal application. This program is located in
`Applications/Utilities/Terminal.app`. You can also search for it with
spotlight.

Once you open it, it should look a bit like this:

![terminalPic](images/terminal.png)

Type in `gcc` and press enter.

A window should pop up:

![installTools](images/install_xcode.png)

Click install and wait while the tools are installed. Once it is done
type the same command again (`gcc` and then enter). If you see

![gccPicture](images/gcc.png)

then everything was installed correctly.

# Installing Homebrew

[Homebrew](http://brew.sh/) (or Brew for short) is a package manager for OS X. 
It lets you easily install software that Apple does not provide by default.

To install it, make sure you have Terminal open. Then paste in:

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

And press enter. It should let you know what it is doing as it installs. You may also have
to enter your password.

**When you enter your password, you will not be able to see the characters being typed and
your cursor won't move. This is for security reasons. Don't worry, you are still typing in the password.**

Once it's done, you can test it by installing a program called `wget`.

Type
```
brew install wget
```
and press enter.

You should see

![wgetInstall](images/wget.png)

# Using Homebrew to Update Git

The Git that the Xcode Command Line tools provides is fairly out of date
(1.7 vs 2.5). Now that you have Homebrew installed, you can get a more up-to-date
version of Git.

Run the command
```
brew install git
```

Now you have 2 versions of Git installed. The default Mac version is installed in
a folder called `/usr/bin`, but Homebrew installed another version in `/usr/local/bin`.
We want to use the version Homebrew installed. To do this, run the following two
commands:
```
echo 'export PATH=/usr/local/bin:$PATH' >> ~/.bash_profile
```
```
source ~/.bash_profile
```

These commands may be confusing, but in short, what they do, is make your computer
check `/usr/local/bin` for the Git program before checking `/usr/bin`.
