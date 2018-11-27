# Ryan's Mac Dev Setup

## Install the following Software

- General software update

    softwareupdate -ia

- Install Brew

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

- Install Command Line Tools

    xcode-select --install

- Install VSCode

    Install the `settings sync` extension

## Brew Packages and configuration

brew install

    brew install git && brew link --overwrite git
    brew install bash-completion
    brew install dockutil
    brew install direnv
    brew install google-chrome
        dockutil --add /Applications/Google\ Chrome.app
    brew cask install slack
        dockutil --add /Applications/Slack.app
    brew cask install iterm2
        dockutil --add /Applications/iTerm.app	
    brew install python3
    brew cask install spectacle
        configure appropriately
    brew cask install postman 
        dockutil --add /Applications/Postman.app
    brew cask install spotify
        dockutil --add /Applications/Spotify.app

## Keys and Security

- Install and configure Password Managers (1Password, LastPass)
- Configure Github

    git config --global user.name "Firstname Lastname"	
    git config --global user.email "foo@bar.com"

    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    eval "$(ssh-agent -s)"
    vim ~/.ssh/config
        >>> Host *
         >>>    AddKeysToAgent yes
         >>>    UseKeychain yes
         >>>    IdentityFile ~/.ssh/id_rsa
    ssh-add -K ~/.ssh/id_rsa
    less ~/.ssh/id_rsa.pub | pbcopy
    paste into github settings with new machine name
