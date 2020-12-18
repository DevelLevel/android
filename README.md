<p align="center">
<img src="https://github.com/AospExtended/manifest/raw/7.1.1/aex_logo.png" width="320px" height="320px" > 
</p>

AospExtended Nougat
===========
AospExtended is just an extension to AOSP, through which we 
are trying to provide a stock AOSP experience along with some important 
customization features. We have cherry-picked the features from many 
other projects and hence we are very thankful to them.

Credits
-------
* [**JDCTeam (Base)**](https://github.com/AOSP-JF-MM)
* [**DirtyUnicorns**](https://github.com/DirtyUnicorns)
* [**AOSiP**](https://github.com/AOSIP)
* [**ZephyrOS**](https://github.com/Zephyr-OS)
* [**TurboROM**](https://github.com/TurboROM)
* [**TeamSubstratum (Theme Engine)**](https://github.com/Substratum)
* [**SlimRoms**](https://github.com/SlimRoms)
* [**BlissRoms**](https://github.com/BlissRoms)
* [**LineageOS/Cyanogenmod**](https://github.com/LineageOS)
* [**Nitrogen Project**](https://github.com/nitrogen-project)
* [**Pure Nexus**](https://github.com/PureNexusProject)
* [**GZR Community**](https://plus.google.com/communities/109330559573276360638)
* [**OmniROM**](https://github.com/omnirom/)
* [**AOSPA**](https://github.com/aospa/)
* [**ABC ROM**](https://github.com/ezio84)

Packages needed?
-------------

To build AOSP do you need to prepair your macheine:

```bash
  --Taken from xda: https://forum.xda-developers.com/android/general/build-aosp-extended-ubuntu-18-04-bionic-t3796500--
  
1. Add this line to /etc/apt/sources.list

deb http://cz.archive.ubuntu.com/ubuntu trusty main

2. Get packages

sudo apt-get update

mkdir -p ~/bin

wget 'https://storage.googleapis.com/git-repo-downloads/repo' -P ~/bin

chmod +x ~/bin/repo

sudo apt-get install openjdk-8-jdk android-tools-adb bc bison build-essential curl flex g++-multilib gcc-multilib gnupg gperf imagemagick lib32ncurses5-dev lib32readline-dev lib32z1-dev libesd0-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libwxgtk3.0-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc yasm zip zlib1g-dev git-core python screen

3. Setup git

git config --global user.name "your name"

git config --global user.email "your email"

4. Add repo path and enable ccache

nano ~/.bashrc

Add these lines to the bottom of bashrc

export PATH=~/bin:$PATH
export USE_CCACHE=1
export LC_ALL=C

Then to enable these use command

source ~/.bashrc
```

How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a 
command like this:

```bash
  repo init -u git://github.com/DevelLevel/android_manifest-AEX.git -b 7.x
```
  
Then to sync up:
----------------

```bash
  repo sync -c -jx --force-sync --no-clone-bundle --no-tags
```
Finally to build:
-----------------

```bash
  . build/envsetup.sh
  lunch aosp_device_codename-userdebug
  make aex -jx
```

