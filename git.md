## Using Homebrew to Update Git

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

Now if you run
```
git --version
```
You should see
```
git version 2.5.0
```
