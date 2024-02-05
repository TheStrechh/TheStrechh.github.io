---
hide:
  - navigation
---

# LineageOS For Xiaomi Poco X5 Pro (redwood)

- You can find `UNOOFFICIAL` LineageOS 21 builds [`HERE`](https://sourceforge.net/projects/thestrechh/files/redwood/lineage-21/)
- Current version: LineageOS 21 (Android 14)
- Build type: Vanilla

## Flashing additional partitions (Only if it's the first time, coming from a MIUI or another CustomROM)

!!! note
    * No, you can't flash back TWRP or any other custom recoveries, overwise OTA updates would break.
    * Follow every comment of this guide to avoid issues while you flash any Custom Rom by me.
    * Don't continue if any of these steps fails.

- Download the following files from [`HERE`](https://sourceforge.net/projects/thestrechh/files/redwood/lineage-21/recovery/).
- Power off the device, and boot it into bootloader mode:
	- With the device powered off, hold Volume Down + Power. Keep holding both buttons until the word `FASTBOOT` appears on the screen, then release.
- Flash the downloaded image files to your device by typing:
``` bash
	fastboot flash dtbo dtbo.img
	fastboot flash vendor_boot vendor_boot.img
	fastboot flash boot boot.img
``` 
- Now reboot into recovery to verify the installation.
	- With the device powered off, hold Volume Up + Power. Keep holding both buttons until the `MI` logo appears on the screen, then release.

## Installing LineageOS from recovery (coming from a MIUI, another CustomROM or if you want clean flash)

- Download the LineageOS installation package that you would like to install or build the package yourself.
    - (Optionally): If you want to install an application package add-on such as Google Apps (use the arm64 architecture), please read and follow the instructions on Google Apps page
- If you are not in recovery, reboot into recovery:
    - With the device powered off, hold Volume Up + Power. Keep holding both buttons until the `MI` logo appears on the screen, then release.
- Now tap Factory Reset, then Format data / factory reset and continue with the formatting process. This will remove encryption and delete all files stored in the internal storage, as well as format your cache partition (if you have one).
- Return to the main menu.
- Sideload the LineageOS .zip package:
    - On the device, select `Apply Update`, then `Apply from ADB` to begin sideload.
    - On the host machine, sideload the package using: ``` adb sideload lineage-20.0-xxxxxxxx-UNOFFICIAL-redwood.zip``` and ```adb sideload fw_redwood_miui_REDWOODRUGlobal_VXX_X_X_X_XXXXXX_XXXXXXXXXX_13.zip```
- (Optionally): If you want to install any add-ons, repeat the sideload steps above for those packages in sequence.
- Once you have installed everything successfully, click the back arrow in the top left of the screen, then `Reboot system now`.

## Dirty Flash LineageOS from recovery (updating from previous build)

- Now reboot into recovery.
	- With the device powered off, hold Volume Up + Power. Keep holding both buttons until the `MI` logo appears on the screen, then release.
- Sideload the LineageOS .zip package:
    - On the device, select `Apply Update`, then `Apply from ADB` to begin sideload.
    - On the host machine, sideload the package using: ``` adb sideload lineage-20.0-xxxxxxxx-UNOFFICIAL-redwood.zip``` and ```adb sideload NikGapps-xxxxx-arm64-13-xxxxxxxx-signed.zip```
- Once you have installed everything successfully, click the back arrow in the top left of the screen, then `Reboot system now`.

## Extras Flash (Gapps, Magisk, ...) if any
!!! warning
    Gapps package MUST be flashed before booting into the OS, don't blame me if internet doesn't work on Play Store or something.

* Sideload the remaining zip files (Gapps, Magisk, ...) (Ignore any `Signature verification failed` errors in this stage).

``` bash
    # On the device, Tap `Apply update`, then `Apply from ADB` for starting the sideload service
    # On the computer, sideload the package using this command (Mention the path of the extra zips before running the command):
    # Ex: adb sideload /home/thestrechh/redwood/Magisk.zip
    adb sideload <extra>.zip
```

## About Device

The Xiaomi Poco X5 Pro 5G (codenamed _"redwood"_) is a mid-range smartphone from Xiaomi.
It was released in February 2023.

## Device specifications

| Device                  | Xiaomi Poco X5 Pro                                                       |
| ----------------------- | :----------------------------------------------------------------------- |
| SoC                     | Qualcomm Snapdragon 778G 5G (SM7325-2-AB)                                |
| CPU                     | Kryo 670, Up to 2.4 GHz, Octa-core CPU                                   |
| GPU                     | Adreno 642L                                                              |
| Memory                  | 6/8 GB, LPDDR4X                                                          |
| Shipped Android Version | 12                                                                       |
| Storage                 | 128/256 GB, UFS 2.2                                                      |
| Battery                 | Non-removable 5000 mAh                                                   |
| Display                 | 2400 x 1080 pixels, 6.67 inches                                          |
| Camera                  | 108 MP main, 8 MP ultra-wide angle, 2 MP telemacro, 16 MP front          |