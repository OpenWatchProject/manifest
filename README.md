# Android 10 Openwatch manifest #

### Setup build enviroment ###
https://source.android.com/setup/build/initializing#installing-required-packages-ubuntu-1804

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/OpenWatchProject/manifest -b android-10

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

$ python vendor/mediatek/proprietary/scripts/releasetools/split_build_helper.py full_c7s-userdebug

```

The above command will give you 3 commands that are customized for the product and eng/userdebug/user you specfied

Note: Atleast on mt6739 building with eng made the device almost unusable due to the lag.
