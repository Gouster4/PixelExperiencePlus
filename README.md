# Pixel Experience Plus #


### Prepare ###

```bash

# install packages
sudo apt-get install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev libgl1-mesa-dev libxml2-utils xsltproc unzip

```


```bash

# create directory
mkdir ~/android
cd ~/android

```

```bash

# The Android build process expects python to be python2. Prepend it to the PATH
$ mkdir bin
$ ln -s /bin/python2 bin/python
$ export PATH=$PWD/bin:$PAT

```


### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/Gouster4/PixelExperiencePlus -b ten-plus

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -j$(nproc --all)
```

### Difference from Pixel Experience Plus ###

Eleven - LineageOS music player  

AudioFX - LineageOS equalizer

Recorder - LineageOS Screen and sound recorder
