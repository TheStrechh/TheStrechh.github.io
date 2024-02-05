---
hide:
  - navigation
---

# Troubleshooting

During your use of LineageOS, crDroid or DerpFest, you may encounter some unexpected issues.

I can't do much about these unless appropriate logs are given.

!!! note
    I will not assist if any modification is made to the ROM: For example, if a different kernel is flashed, if random Magisk modules are installed, or if the ROM is flashed with a different recovery.

## Report an issue

To properly report an issue, the following logs must be provided in the ticket:

- `logcat` (System Log).
- `dmesg` (Kernel Log).

### Logcat

To grab a `logcat` it is required to have `USB debugging` enabled:

* Go into `Settings` -> `About Phone` and press 7 times the `Build Number`.
* Go into `Settings` -> `System` -> `Developer options` and enable `USB Debugging`.
* Open an `ADB & Fastboot tools` window on your PC and run this:

``` bash
    adb logcat -d > logcat.log
```

* If a radio buffer log is requested, run this as well:

``` bash
    adb logcat -db radio > radio.log
```

### Dmesg

Grabbing a `dmesg` requires root access. Fortunately, userdebug builds of LineageOS can access a root shell enviroment out-of-the box:

* Go into `Settings` -> `About Phone` and press 7 times the `Build Number`.
* Go into `Settings` -> `System` -> `Developer options` and enable `USB Debugging` and `Rooted debugging`.
* Open a `ADB & Fastboot tools` window on your PC and run this:

``` bash
    adb root # Enables root shell
    adb shell dmesg > dmesg.log
```
