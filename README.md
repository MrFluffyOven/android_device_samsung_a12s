## Recovery Device Tree for the Samsung Galaxy A12S [SM-A127F]

# How-to compile it:

## twrp 12.1 Manifest
    repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
## Sync
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
## Clone twrp tree
    git clone https://github.com/MrFluffyOven/android_device_samsung_a12s -b twrp-12.1 device/samsung/a12s
## build:
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_a12s-eng; mka recoveryimage
## Multidisabler
    Boot twrp, Wipe data, Reboot Recovery, go to twrp terminal, type "multidisabler" hit enter/return , Wipe data again, Encryption should be Disabled
