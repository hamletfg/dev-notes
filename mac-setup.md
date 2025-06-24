# Mac Dev Setup

### Set up Homebrew
First thing is to set up Homebrew to install some of the other programs through the terminal. The thing that kept throwing me off when I first started installing Homebrew was that it would give me an error of `zsh:command not found: brew` upon further investigation, I was missing a critical step on reading the last two lines that Hombrew would give me after the install in the terminal. 

A good reference is [Install Homebrew](https://mac.install.guide/homebrew/3) by the Mac Install Guide

### Install Git using Homebrew
Git is typically installed as part of Xcode Command Line Tool, but installing through Homebrew often provides a more up-to-date version of Git compared to Xcode Command Line Tools. 

You can install Git by running `brew install git`.

### Configure Git

Follow [Odin Project Guide](https://www.theodinproject.com/lessons/foundations-setting-up-git) for Git Setup Guide

### Install nvm using Homebrew

1. Install `nvm` using Homebrew:
```
brew install nvm
```
2. Create the necessary directories for nvm:
```
mkdir ~/.nvm
```
3. Update your shell configuration file (.zshrc for Zsh, which is the default shell on macOS):
```
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"' >> ~/.zshrc
echo '[ -s "/opt/homebrew/opt/nvm/etc/bash_completion" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion"' >> ~/.zshrc
```
4. Source your shell configuration file to apply the changes:
```
source ~/.zshrc
```
5. Verify the installation by checking the nvm version:
```
nvm --version
```

### Install npm using nvm

1. Install the desired version of Node.js using nvm. For example, to install the latest LTS version:
```
nvm install --lts
```
2. Verify the installation of Node.js and npm:
```
node -v
npm -v
```
3. Use a specific version of Node.js if you have multiple versions installed. For example, to use the latest LTS version:
```
nvm use --lts
```

### Open VS Code From the Terminal

The guide is on [freeCodeCamp](https://www.freecodecamp.org/news/how-to-open-visual-studio-code-from-your-terminal/)
