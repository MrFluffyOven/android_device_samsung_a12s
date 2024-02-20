## Recovery Device Tree for the Samsung Galaxy Tab A8 [SM-X200]

# How-to compile it:

## twrp 12.1 Manifest
    repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
## Sync
    repo sync
## Clone Magendanz twrp tree
    git clone https://github.com/MrFluffyOven/gta8wifi_magendanz_fork.git -b twrp-12.1 device/samsung/gta8wifi
## build:
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_gta8wifi-eng; mka recoveryimage
## Multidisabler
    Boot twrp, Wipe data, Reboot Recovery, go to twrp terminal, type "multidisabler" hit enter/return , Wipe data again, Encryption should be Disabled
