# Local Manifest
Local Manifest for syncing device sources with repo
# Guide to ROM building

You can use this guide to build any ** Custom Rom** you want.


# Setup Building Environment

## Install Packages (Ubuntu 20.04)

- Let's Install necessary Packages
	> sudo su
	
	> add-apt-repository ppa:openjdk-r/ppa
	
	> apt-get update

	> apt install openssh-server screen python git openjdk-8-jdk android-tools-adb bc bison \
	build-essential curl flex g++-multilib gcc-multilib gnupg gperf imagemagick lib32ncurses-dev \
	lib32readline-dev lib32z1-dev  liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev \
	libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc yasm zip zlib1g-dev \
	libtinfo5 libncurses5

	> exit
## Install Repo

> mkdir ~/bin
	
> PATH=~/bin:$PATH

> cd ~/bin

> curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

> chmod a+x ~/bin/repo
## Run Setup scripts

> git clone https://github.com/akhilnarang/scripts.git scripts

> cd scripts

> bash setup/android_build_env.sh
## Let's Cook ROM
- Here after changes should be made accordingly.
> git config --global user.name "Santhanabalan" && git config --global user.email "bala2102002@gmail.com"

> mkdir rom

> cd rom

> repo init 
- I pushed all my repositories to GitHub/GitLab and I am using manifest to track all of them.

> cd .repo

> git clone https://github.com/Santhanabalan/local_manifests -b rom

> cd ../

> repo sync