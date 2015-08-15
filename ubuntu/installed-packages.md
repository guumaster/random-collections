## Ubuntu info


### Get a list of manualy installed packages

```sh
comm -23 <(apt-mark showmanual | sort -u) <(gzip -dc /var/log/installer/initial-status.gz | sed -n 's/^Package: //p' | sort -u)
```
### My common packages list

```
build-essential
curl
dkms
docker.io
flashplugin-installer
git
git-extras
google-chrome-stable
haroopad
heroku-toolbelt
htop
libasound2-dev
libzmq3-dev
mongodb
nodejs
openssh-server
oracle-java8-installer
oracle-java8-set-default
robomongo
tmux
vim
vim-gnome
vim-syntax-docker
virtualbox-guest-dkms
virtualbox-guest-utils
virtualbox-guest-x11
zsh
```


### Extra sources.list

```
docker.list
deb https://get.docker.com/ubuntu docker main

google-chrome.list
### THIS FILE IS AUTOMATICALLY CONFIGURED ###
# You may comment out this entry, but any other modifications may be lost.
deb http://dl.google.com/linux/chrome/deb/ stable main

heroku.list
deb http://toolbelt.heroku.com/ubuntu ./

heroku.list.save
deb http://toolbelt.heroku.com/ubuntu ./

mongodb.list
deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen

mongodb.list.save
deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen

nodesource.list
deb https://deb.nodesource.com/node utopic main
deb-src https://deb.nodesource.com/node utopic main

nodesource.list.save
deb https://deb.nodesource.com/node utopic main
deb-src https://deb.nodesource.com/node utopic main

virtualbox.list
deb http://download.virtualbox.org/virtualbox/debian trusty contrib
deb http://download.virtualbox.org/virtualbox/debian saucy contrib
deb http://download.virtualbox.org/virtualbox/debian raring contrib
deb http://download.virtualbox.org/virtualbox/debian quantal contrib
deb http://download.virtualbox.org/virtualbox/debian precise contrib
deb http://download.virtualbox.org/virtualbox/debian lucid contrib non-free
deb http://download.virtualbox.org/virtualbox/debian wheezy contrib
deb http://download.virtualbox.org/virtualbox/debian squeeze contrib non-free


webupd8team-ubuntu-java-utopic.list
deb http://ppa.launchpad.net/webupd8team/java/ubuntu utopic main
# deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu utopic main
```
### Mount workspace vdi on VirtualBox

#### Add user to vboxsf group 
`sudo adduser $USER vboxsf`

#### Mount drive in `/etc/fstab`
Get  the drive UUID with  `sudo blkid` and add it to `/etc/fstab`

`UUID=<your_disk_uuid> /home/workspace auto nosuid,nodev,nofail,x-gvfs-show 0 0`

#### Change access
If you get access errors, change ownership

```sh
sudo chmod -R a+rwX,o-w /home/workspace
sudo chown -R $USER:$USER /home/workspace
```


