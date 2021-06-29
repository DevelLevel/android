<p align="center">
<img src="https://raw.githubusercontent.com/AospExtended/Documentation_and_thread-template/10.x/Banner.png" > 
</p>

AospExtended Eleven (For Suzuran)
===========
AospExtended is just an extension to AOSP, through which we 
are trying to provide a stock AOSP experience along with some important 
customization features. We have cherry-picked the features from many 
other projects and hence we are very thankful to them.

Credits
-------
* [**JDCTeam**](https://github.com/AOSP-JF-MM)
* [**DirtyUnicorns**](https://github.com/DirtyUnicorns)
* [**TeamSubstratum (Theme Engine)**](https://github.com/Substratum)
* [**LineageOS/Cyanogenmod**](https://github.com/LineageOS)
* [**Nitrogen Project**](https://github.com/nitrogen-project)
* [**ABC ROM**](https://github.com/ezio84)
* [**GZOSP**](https://github.com/GZOSP)
* [**Pure Nexus**](https://github.com/PureNexusProject)
* [**OmniROM**](https://github.com/omnirom/)
* [**AOSPA**](https://github.com/aospa/)
* [**BlissRoms**](https://github.com/BlissRoms)

Setting up the environment! (on Rocky Linux 8.4)
-------------

Install packages:
```bash
  sudo dnf install epel_release
  sudo dnf install screen git vim python3 libncurses* gcc gcc-c++ kernel-devel make ccache
```

Install REPO:
```bash
  mkdir ~/bin
  curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
  chmod a+x ~/bin/repo
```

Configure GIT:
```bash
  git config --global user.name "your name"
  git config --global user.email "your email"
```

Configure .bashrc:
```bash
  # edit ~/.bashrc and add
  
  export PATH=~/bin:$PATH
  export USE_CCACHE=1
  export LC_ALL=C
  
  # save and run:
  source ~/.bashrc
```

Configure python:
```bash
  sudo ln -s /usr/bin/python3 /usr/bin/python
```

How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a 
command like this:

```bash
  repo init -u git://github.com/AospExtended/manifest.git -b 11.x
```
To initialize a shallow clone, which will save even more space & time, use a command like this:

```bash
  repo init --depth=1 -u git://github.com/AospExtended/manifest.git -b 11.x
```
  
Then to sync up:
----------------

```bash
  repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
Finally to build:
-----------------

```bash
  source build/envsetup.sh
  lunch aosp_device_codename-userdebug
  m aex -j$(nproc --all) | tee log.txt
```
## Report build issues
- You can reach us via [Telegram](https://t.me/aospextendedgroup)

## Maintain Officially
- If you're building **AospExtended** for an unofficial device and would like to make it official, Check out the link below for more information about the requirements for both you and your device.  
- [Click here for more info](https://github.com/AospExtended/Documentation_and_thread-template) (**Read full README**)

### Important Links:

- [Website](http://www.aospextended.com/)
- [Download Center](https://downloads.aospextended.com/)
- [Blog](https://blog.aospextended.com/)
- [Gerrit Code Review](http://gerrit.aospextended.com/)
- [Telegram Channel](https://telegram.me/aospextended/)
- [Documentation & Thread Template](https://github.com/AospExtended/Documentation_and_thread-template/) 
- [Help us translate AospExtended ROM and bring it to the world!](http://translate.aospextended.com/)
- [Theme Resources](https://github.com/AospExtended/AEX-Scripts/) 
- [Extended Devices](https://github.com/AospExtended-devices/)
- [Gallery](https://aospextended.com/gallery)
- [Facebook page!](https://www.facebook.com/aospextended/)
