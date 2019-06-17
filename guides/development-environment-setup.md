# Development Environment Setup

We will be installing the following tools in our development environments and we will get familiar with bash:

- A package manager (`apt-get` on Linux, home`brew` on Mac)
- Install `curl`
- Install `git` and configure it
- Install Sublime Text 3
- Install NVM (Node Version Manager) and use it to install Node
- Get familiar with Bash Commands


## Using Your Package Manager

Package managers are client applications that allow us to install, upgrade, configure, and remove programs and libraries on our computers. They ensure that all necessary dependencies are automatically installed and configured correctly. We will use these to install various packages during our program and you will probably use these extensively in your careers.


**Mac Users:**

Mac users should ensure they have installed both XCode and [Homebrew](https://brew.sh/). Once this has been completed, you can use the `brew` command to install packages. Try the following to ensure brew is working correctly.

```bash
brew update
brew install curl
```

**Note:** anytime you want to install a package, you should first run the `brew update` command. This downloads the latest package manager index files, which lets brew know of the latest available packages and versions.


**Lubuntu Users:**

The Debian/Ubuntu package manager is `apt-get`. Run the following commands to install the `curl` and `build-essential` packages.

```bash
sudo apt-get update
sudo apt-get install curl build-essential
```

**Note:** anytime you want to install a package, you should first run the `sudo apt-get update` command. This downloads the latest package manager index files, which lets apt-get know of the latest available packages and versions.


## Git

**Mac Users:**

```bash
brew update
brew install git
```

**Lubuntu Users:**

```bash
sudo apt-get update
sudo apt-get install git
```

### One Time Configuration

You should always configure git and let it know who you are the first time you install it on a new machine. This way the commit log will always have proper author information.

```bash
git config --global user.name "First Last"
git config --global user.email "my@email.com"

git config --global push.default simple
git config --global core.autocrlf input
```

#### Explanation of the final two commands

```bash
git config --global push.default simple
```

This tells git to only push updates from your current branch up to remote repositories (like github). If you don't do this, then the original behavior could be to push all branches, even your experimental ones, up to remote repositories.

```bash
# mac/linux
git config --global core.autocrlf input
# windows only
git config --global core.autocrlf true
```

This setting deals with the end of lines (EOL) in your code files. For the best compatibility across platforms, it is best if windows users set this to `true` and Mac/Linux users set this to `input`.


## Sublime Text 3

You are free to use any text editor that supports JavaScript, such as: vim, emacs, Sublime Text, Atom, Textmate, Visual Studio Code.

Below are instructions for the installation of the Sublime Text editor.

**Mac Users:**

Mac users can download Sublime Text directly from the Sublime website [https://www.sublimetext.com/3](https://www.sublimetext.com/3) and follow the installation instructions.

_Setting up the `subl` command line tool_ If you would like to launch sublime from the command line on OS X you will have to set it up with the following command:

```bash
ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

**Lubuntu Users:**

Lubuntu/Ubuntu users can use `apt-get` to install Sublime Text. The following commands are detailed here: [https://www.sublimetext.com/docs/3/linux_repositories.html#apt](https://www.sublimetext.com/docs/3/linux_repositories.html#apt)

```bash
# Install the GPG Key
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -

# Use the stable channel
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

# Install Sublime Text
sudo apt-get update
sudo apt-get install sublime-text
```

`apt-get` will now be able to update sublime-text like any other package.

The Sublime Text editor can now be launched with the `subl` command or via the application menu in Lubuntu.


## NVM and Node

The best way to manage your Node.js installations is to use the NVM (Node Version Manager) tool. It allows you to have multiple versions of Node.js installed simultaneously and provides commands to easily switch between different versions.

```bash
# Mac users should run this command first
touch ~/.bash_profile

# Install nvm (both linux and mac users)
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash

# After nvm installs you should close your terminal and open a new one to access nvm

# Verify that nvm is working
nvm ls

# Install the LTS node.js version
nvm install 8.11.4

# Install another node.js version
nvm install 10.9.0

# You are now using version 10.9.0, to switch back to 8.11.4 run
nvm use 8.11.4

# Run the node repl (read-eval-print loop)
node
```

The `node` command runs the interpreter allowing you to run and evaluate JavaScript code. This is similar to running the `python`, `ruby`, or `php` interpreters on the command line, if you are familiar with those languages.

**Exiting Node:** Press `ctrl+d`

If the nvm command is not working for you on the Mac, then check this section for additional troubleshooting: [https://github.com/creationix/nvm#install-script](https://github.com/creationix/nvm#install-script).


## Basic Command Line Commands

### Open your terminal

**Mac Users:** can press `CMD+SPACE` and type "terminal" to launch it.

**Lubuntu Users:** can click on the bottom left corner icon on the Desktop. This will bring up the Program menu. You will find "LXTerminal" under the System Tools folder in the Program menu.

### Command Descriptions

`pwd`: print working directory

`ls`: list directory

`mkdir`: make directories

`cd`: change working directory

`touch`: change file timestamps, or create empty file if it doesn't exist.

`ls -l`: use long format for directory listings

`cd ..`: change to parent directory

`mv`: move file command is used to both move and/or rename files

`cp`: copy file command

`rm`: remove file command

I recommend using the [https://explainshell.com/](https://explainshell.com/) website to learn about commands and their various options, especially when you find you are being asked to run commands you are not familiar with.

If you are new to the command line and want to learn more, you can start by taking the following codecademy course: [https://www.codecademy.com/learn/learn-the-command-line](https://www.codecademy.com/learn/learn-the-command-line).

