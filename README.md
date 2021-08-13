# rt-ubuntu-dell-xps13-9310

* adventures in making ubuntu work for me on a dell xps 13 9310
* lots of this stuff will probably be an edge case because i migrated from WSL on a surface book 2, see https://github.com/rtanglao/rt-making-wsl-and-windows-work-for-me/blob/master/README.md

## 13august2021 how to make tresorit linux app bigger in Ubuntu 20.04

* Edit `/home/roland/.local/share/applications/tresorit.desktop`
* Change `Exec=/home/roland/.local/share/tresorit/tresorit %u to``Exec=env QT_SCREEN_SCALE_FACTORS=2 /home/roland/.local/share/tresorit/tresorit %u`

## 26april2021 how to change the terminal title
* from [How to change Gnome-Terminal title?](https://askubuntu.com/questions/22413/how-to-change-gnome-terminal-title)
```bash
PS1='\[\e]0;newtitle\a\]${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
```

## 19april2021 how to install Imagemagick on Ubuntu 20.04 with JPG, PNG and TIFF delegates
* why isn't this the default install
[Install ImageMagick with JPG, PNG and TIFF Delegates - Ubuntu (20.04)](https://gist.github.com/nickferrando/fb0a44d707c8c3efd92dedd0f79d2911)

## 16april2021 install cmake to install gollum for the gitlab wiki
```bash
sudo apt-get install cmake
gem install gollum
```
## 05pril2021 firefox extern extension that only works with linux, use gedit or any other editor to edit text areas in firefox with shift control d
* https://addons.mozilla.org/en-US/firefox/addon/textern/
## 22february 2021 getting pip3

```bash
sudo apt-get install software-properties-common
sudo apt-add-repository universe
sudo apt-get update
sudo apt-get install python3-pip
```

## 15february2021

* reinstalled but made sure it was encrypted when erasing disk
* sudo apt install gnome-tweak-tool
* install dash to panel gnome extension

## 13january2021 getting ssh to work


* I googled "No more authentication methods to try." and found the 
answer here: https://askubuntu.com/questions/343060/no-more-authentication-methods-to-try-permission-denied-publickey
  * Perhaps I messed up and this isn't necessary or it's only necessary because i copied the `.ssh` directory from WSL on a surface book 2?

```
sudo chmod 700 ~/.ssh/
sudo chmod 600 ~/.ssh/*
sudo chown -R User ~/.ssh/
sudo chgrp -R User ~/.ssh/
sudo chmod 700 ~/.ssh/controlmaster

where User===roland in my case
```
