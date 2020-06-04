👨‍💻 Development environment setup after a clean Mac OS install
===================

This is what is use as a playground. I mainly do full stack js with react / meteor / raw node and sometimes ember. I also go for some mative apps ios/android some go and some rust. Sometimes python and some PHP legacy code. Mongo Aerospike and sql for databases.

At first, check updates via the appstore.

> To add a temporary directory to the PATH, run `export PATH="__folder__:$PATH"` ; to add a permanent directory to the PATH, `nano ~/zshrc` and add `export PATH="__folder__:$PATH"`

Display hidden folders :
* run `defaults write com.apple.finder AppleShowAllFiles YES`
* run `killall Finder` to restart the finder

## 📖 Table of Contents

- [Basic settings](#-basic-settings)
- [Get the `/usr/local` ownership](#-get-the-usrlocal-ownership)
- [Install your package manager: Homebrew](#-install-your-package-manager-homebrew)
- [Configure Git](#-configure-git)
- [Get a better terminal](#-get-a-better-terminal)
- [Install broswers](#-install-broswers)
- [Install some global packages and utilities](#-install-some-global-packages-and-utilities)
- [Install MAMP](#-install-mamp)
- [Install Docker](#-install-docker)
- [Create a partition for your projects](#-create-a-partition-for-your-projects)
- [Get your editor ready: VSCode](#-get-your-editor-ready-vscode)
- [Other applications](#-other-applications)

## 🖥 Basic settings

In the system preferences

* general
	* icon size > small
	* Use dark menu bar and dock
* desktop > choose a nice wall paper !
* dock
	* small size, small magnifiying
	* bottom
	* hide automatically
* mouse / trackpad
	* desactivate natural way
	* tap to click and two tap to right clic

In the finder preferences

* General: check everything
* Sidebar: what you like
* Advanced: check everything

## 👤 Get the `/usr/local` ownership

  sudo chown -R $USER /usr/local

> This will make you owner of your /usr/local folder. [Important for npm use.](http://foohack.com/2010/08/intro-to-npm/#what_no_sudo) and necessary for proper homebrew use.

## 🍺 Install your package manager: Homebrew

This will help installing command line programs. 

Run: `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

On a mac, you have ruby.

> Don't `sudo`. You have the ownership of your `/usr/local` folder.

Install a few packages :

* `brew install git`
* `brew install wget`
* `brew install mysql`
* `brew install mongo`
* `brew install nvm`=> node version manager <https://github.com/nvm-sh/nvm>
* `brew install yarn` => replacement for the npm command (install once node is installed)

📌 You should now install node with nvm

> nvm is super important, you should install node with nvm to be able to manage your node versions

## 🐨 Configure Git

You installed it with `brew install git`. Now, configure your git credentials :

    git config --global user.name "fabien"
    git config --global user.email "fabien.huet@gmail.com"

Create SSH key (with no passphrase, this is just a useless pain):

    ssh-keygen -t rsa -b 4096 -C "fabien.huet@gmail.com"

Then copy it with :

    pbcopy < ~/.ssh/id_rsa.pub

Then add it to github, bitbucket, gitlab... accounts.

Make git case sensitive

	git config --global core.ignorecase false

## <~/> Get a better terminal

1. Install iterm 2 <http://www.iterm2.com/> , then open preferences
2. Uncheck « Native full screen windows » in « General »
3. Add ctrl + esc as hotkey to make it appear in « Keys »
4. Go full screen ( cmd + return )
5. Install oh-my-zsh : `curl -L http://install.ohmyz.sh | sh` and restart the terminal
6. Make it Launch on startup in `/system preferences/Users & Groups/Login Items`
7. In the iterm menu /Iterm2/Make Iterm2 default term
8. Download and install the patched version of inconsolata from [powerline fonts](https://github.com/powerline/fonts)
9. Set it as default font for ascii and non ascii characters (12pt) in your iterm prefrences/Profiles/Text/Change font
10. Install [agnosterzak](https://github.com/zakaziko99/agnosterzak-ohmyzsh-theme) and set `ZSH_THEME="agnosterzak"` in `~/.zshrc` (`nano ~/.zshrc` to start editing) and add the custom fonts
11. Install Mac port to get the linux commands : <https://www.macports.org/>
12. pick a colour theme : <http://iterm2colorschemes.com/> (« Solarized Dark Higher Contrast" or « Ocean")

## 🌐 Install broswers

Get chrome and firefox. Add some extensions to chrome :

* ublock origin
* advanced rest client
* livereload
* markdown here
* page speed
* panda
* distractoff
* lighthouse

##  📦 Install some global packages and utilities

These are some of the packages you may need:

* Install tldr : `yarn global add tldr` => this is a nice community managed man page simplificator <https://tldr.sh/>
* Install gulp : `yarn global add gulp`
* Install webpack : `yarn global add webpack`
* Install eslint : `yarn global add eslint` => <https://github.com/roadhump/SublimeLinter-eslint>
* Install meteor : `curl https://install.meteor.com/ | sh`
* Install ack : `brew install ack` => replacement for grep <https://beyondgrep.com/>
* Install tree : `brew install tree` => tree command from linux <https://linux.die.net/man/1/tree>
* Install broot : `brew install broot` => a better tree command (really better, use it!) <https://dystroy.org/broot/>

## 🐘 Install MAMP

Because sometimes, you will need PHP. <http://www.mamp.info/en/downloads/>

## 🐳 Install Docker

Go to https://hub.docker.com/

Start it and go configure it. Allow at least 2 cores and 6 Go (8 is better).

## 💽 Create a partition for your projects

MacOs is not case sensitive by default. So you have to create a partition dedicated to your projects.

Give yourself at least a 100 Go APFS case sensitive partition.

## ✏ Get your editor ready: VSCode

Get VSCode : <https://code.visualstudio.com/>.

Add some extensions:

* Prettier https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
* Chrome debugger https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome
* ESLint https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
* StyleLint https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint
* Docker https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker
* GitLens https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens
* Liveshare https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack

Setup the command line launcher : Open the Command Palette (⇧⌘P) and type `shell command` to find the Shell Command: Install `code` command in PATH command. You can then `code .` to open the current directory in VSCode.

see https://code.visualstudio.com/docs/setup/mac

## 🗂 Other applications

### 📎 Utilities

1. **Dropbox** & **Google drive** To keep your datas safe. <https://www.dropbox.com/?landing=dbv2>, <https://drive.google.com>
2. **Folx** Torrent downloader <https://mac.eltima.com/torrent-client.html>
3. **VLC** Best video player <http://www.videolan.org/vlc/>
5. **OmniDiskSweeper** <https://www.omnigroup.com/more/>
6. **Transmit** for FTP <https://panic.com/transmit/> cyberduck is ok too.
7. **MacDown** to edit markdown <https://macdown.uranusjr.com/>
8. **keepingyouawake** to prevent your mac from going to sleep <https://github.com/newmarcel/KeepingYouAwake> install with `brew cask install keepingyouawake`
9. **SourceTree** for your git client ; Tower is ok too
10. **Robomongo** : <http://robomongo.org/> to manage distant or local mongo database
11. **little snitch** : <https://www.obdev.at/products/littlesnitch/index.html> => manage in and out connections
12. **slack** : <https://slack.com/is> for team communication
13. **Kap** : <https://getkap.co/> video screen capture
14. **CLion** : powerfull IDE for C++ ; xcode is ok too
15. **MS Office suite** to open those files...
16. **skype**
17. **Handbrake** : to compress videos

### 🎨 Graphic / design softwares

The one I use

1. **Photoshop** & **aperture** for pictures
2. **Illustrator** to design elements
3. **Indesign** for documents
4. **Sketch** for interface
5. **Final cut** for video
8. **img optim** to optimize the other images
9. **skyfont** to get google webfonts on my computer

### 📱 Android studio

https://developer.android.com/studio/index.html

### 🔍 Enhance spotlight

Smart move by siong that allow you to shut down / sleep / restart... your mac from spotlight. As you did from Alfred.  https://github.com/siong1987/shortcuts

### 📱 Xcode

You need Xcode. Like it or not. Not only to build iOs / MacOs apps. But also for the command line developper tools. So go there install and accept the licence : <https://itunes.apple.com/fr/app/xcode>.

Note that this is from far the best way to preview a website design on an iphone or an ipad. There are many problem you will just never encounter in chrome that you need to adress. The simulator is perfect for that.
