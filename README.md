# Pixel Experience Plus #

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

LineageOS music player  Eleven

LineageOS equalizer     AudioFX
