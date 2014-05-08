macos setup for web developpement
===================

## Get your terminal ready

1. Install iterm 2 <http://www.iterm2.com/>
2. Uncheck "User Lion-style Fullscreen"
3. Add ctrl + esc as hotkey to make it appear
4. Go full screen
5. Donwload the solarized theme <http://ethanschoonover.com/solarized>
6. Make it Launch on startup in the global mac os preferences
7. Make it default
8. Install oh-my-zsh : `curl -L http://install.ohmyz.sh | sh` and restart the terminal

## Get the /usr/local ownership

  sudo chown -R $USER /usr/local

> This will make you owner of your /usr/local folder. [Important for npm use.]("http://foohack.com/2010/08/intro-to-npm/#what_no_sudo")

## Install broswers

Get chrome, canary and firefox. Add some extensions to chrome :

* adblock plus
* adobe edge inspect
* advanced rest client
* ember inspector
* livereload
* markdown here
* page speed

## Some basic mac os configurations

* Make the invisible files appear

## Install a package manager

Get homebrew :

	ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"

Install a few packages :

* git
* wget
* svn

## Get node and install some basic packages

Get node here : <http://nodejs.org/>

* Install yeoman (you will get grunt and bower) : `npm install -g yo`
* Install meteor `curl https://install.meteor.com/ | sh`

## Install source controll

Get the base git and svn. Then install source tree for Git, the github client and cornerstone for svn.

> Add your new github rsa key to your bitbucket account. Your github acount will setup automatically when syncing with the github client.


## Get your editor ready

Get sublime text : <http://www.sublimetext.com/3>, install the package control packages : <https://sublime.wbond.net/installation> and then some packages :

* advanced new file
* bracket highligther
* colorpicker
* ember snippets
* emmet
* find++
* handlebars
* html5
* javascript snippets
* jquery
* meteor snippets
* scss
* scss snipets
* sidebad enhancements
* sublime linter
* sublime linter jshint
