# Installing Cygwin

Cygwin is a program for Windows that makes it behave
more like Mac and Linux. It gives you a much better
terminal than the one Windows provides and generally
gives you more power than the command prompt.

You can go and download Cygwin from [here](http://cygwin.com/install.html)

I'll also provide some download links:

* [32 bit Cygwin](http://cygwin.com/setup-x86.exe)
* [64 bit Cygwin](http://cygwin.com/setup-x86_64.exe)

Once it downloads, run the exe file. You can leave everything at the default.

It should take some time to install, and once finishes, you should
have a program on your computer called `Cygwin-Terminal`. Open it to
make sure it works (if you see black/white screen with some text then you're good).

# Installing apt-cyg

[Apt-cyg](https://github.com/transcode-open/apt-cyg) is a package manager for Cygwin. 
It lets you install useful software and tools that Windows doesn't provide.

Open a Cygwin Terminal and run it as an administrator (right click and hit *run
as administrator*).

Once the terminal opens, run the following commands:

Type:

```
lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg
```
and press enter. Then type:

```
install apt-cyg /bin
```
and press enter.

It would also be good to install wget, git, and gcc.

Type the following commands:

```
apt-cyg install wget
```
```
apt-cyg install git
```
```
apt-cyg install gcc
```

It's also good to install the text editors Nano and Vim.

```
apt-cyg install nano
```
```
apt-cyg install vim
```

These might take some time to complete. Once they are all done downloading,
type `git` and press enter. You should see a bunch of text appear. If you see

```
bash: git: command not found
```

You didn't install git correctly.
