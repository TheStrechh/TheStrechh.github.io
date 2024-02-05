---
hide:
  - navigation
---

# Download links

The download links for my builds are avaible from my Telegram posts, or from here.

* [`CrDroid for Poco X5 Pro 5G (redwood)`](crdroid/redwood)
* [`DerpFest for Poco X5 Pro 5G (redwood)`](derp/redwood)
* [`LineageOS for Poco X5 Pro 5G (redwood)`](lineage/redwood)

### AOSP Recovery

With every release, I upload also `AOSP Recovery` images:

* `boot.img`
* `vendor_boot.img`
* `dtbo.img`

Download the following files as they are required for the flashing process.

## Firmware

For these builds, I recommend downloading the latest Global Stable firmware to ensure compatibility with the used blobs:

* Poco X5 Pro 5G `redwood`: [`V14.0.7.0.TMSMIXM`](https://xiaomifirmwareupdater.com/archive/firmware/redwood/) `For Android 13/14`

## Google Apps `GApps`

I highly suggest downloading [NickGapps](https://nikgapps.com/) if you want GMS on my vanilla builds builds.

Download the correct package for your installation:

* **Android 14**: [`NikGapps-xxxx-arm64-xx-xxxxxxx-signed.zip`](https://sourceforge.net/projects/nikgapps/files/Releases/NikGapps-U/)
* **Android 13**: [`NikGapps-xxxx-arm64-xx-xxxxxxx-signed.zip`](https://sourceforge.net/projects/nikgapps/files/Releases/NikGapps-T/)

## Extras `Magisk, KernelSU, ...`

* You can safely flash the [latest Magisk release](https://github.com/topjohnwu/Magisk/releases/latest) or without any problems directly from `AOSP Recovery`.
* You can get root without problems, just install the [`latest KernelSU release`](https://github.com/tiann/KernelSU/releases) in your device.

!!! warning
    If you care about banking apps / others that contains root checks, don't flash Magisk since it will break device integrity. That can cause unwanted results such as missing apps on Google Play Store.
