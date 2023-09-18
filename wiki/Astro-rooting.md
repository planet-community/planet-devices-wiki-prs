# Astro: Rooting

To root the Astro Slide, you can use this guide. Overview of the process:

- Back up content from the Astro
- Unlock the Astro's bootloader
- Extract (back up) the stock boot image from the Astro
- Flash a patched boot image to the Astro

## Back up content from the Astro

If you've used the Astro already, **take a backup** of anything you want to keep (photos, apps, data, settings, etc.) as the process described below will wipe it to factory settings (specifically, unlocking the bootloader is what does this).

## Unlock the bootloader

Before following any of the rooting methods below, you need to unlock the bootloader, so the kernel (AKA boot image) that's rooted will be able to boot. Otherwise, the Astro will be soft-bricked if you use an unsigned boot image such as those mentioned below (i.e. anything other than a stock (unmodified) one from Planet Computers).

Use the Astro's bottom/right USB port to connect to your computer.

You can perform the bootloader unlock by following [this iFixit guide](https://www.ifixit.com/Guide/How+to+unlock+the+bootloader+of+an+Android+Phone/152629).

## Find out which slot is currently in use

Android on the Astro uses [Virtual A/B](https://source.android.com/docs/core/ota/virtual_ab) for its OS update mechanism. This means key partitions each have an A and B slot, e.g. `boot_a` and `boot_b`. Only one slot is in use at a time (i.e. all of the `*_a` partitions, or all of the `*_b` partitions), and which slot is active switches over after an OS update is installed to the inactive slot.

To find out which slot you need to operate on for the rest of this guide:

- Reboot to fastboot - run: `adb reboot fastboot`
- Query the current slot: `fastboot getvar current-slot`

This will output something like:

```
current-slot: b
```

**The rest of this document assumes the current slot is A. If it's B, be sure to replace all instances of `_a` with `_b`!**

## Extract (back up) the stock boot image from the Astro

It is strongly recommended to make a backup of your stock boot image, as you'll need to restore it before performing an OTA OS update.

Note that there have been reports of Linux being the easiest OS to get MTKClient working on.

- Install [MTKClient](https://github.com/bkerler/mtkclient), following all the [Linux instructions](https://github.com/bkerler/mtkclient#install)
- Shut down the Astro
- Extract the boot image: `mtk r boot_a boot.img`
- Wait for that to finish, then disconnect
- The image file will have been saved as `boot.img`. Keep a copy of this somewhere safe

## Rooting methods

### Rooting method 1: Use a pre-patched boot image

This method is the easiest, but relies on someone having already published the applicable rooted boot image here, and having to trust that it is not malicious.

- Download the rooted boot image matching your OS version (see Settings -> About phone -> Build number). These rooted boot images were generated using the method: 'Patch the boot image yourself using the Magisk app on Android'
    + V01 (`Astro-11.0-Planet-05182022-V01`)
        * [stock](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v01-stock.img) (md5: `936703a76c8ddd860f2b84b69ae7c951`)
        * [rooted](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v01-magisk-from-app-26300.img) (md5: `b897242ab79dd2accc7d38245c8d3eb7`)
    + V07 (`Astro-11.0-Planet-05192023-V07`)
        * [stock](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v07-stock.img) (md5: `bfa1c0914e8143a2d3cbf9e26a7ad0f6`)
        * [rooted](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v07-magisk-from-app-26300.img) (md5: `bdb8066ad8d3b823dc494b420571fcad`)
    + V07b (`Astro-11.0-Planet-05242023-V07b`)
        * [stock](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v07b-stock.img) (md5: `bfa1c0914e8143a2d3cbf9e26a7ad0f6`)
        * [rooted](https://github.com/shymega/planet-devices/raw/f223dd6f049045ba3042490d34c481454de9af71/resources/boot-images/astro/boot-v07b-magisk-from-app-26300.img) (md5: `bdb8066ad8d3b823dc494b420571fcad`)
- Reboot to fastboot - run: `adb reboot fastboot`
- Flash the image to the Astro - run e.g.: `fastboot flash boot boot-v07b-magisk-from-app-26300.img`
- Reboot: `fastboot reboot`

### Rooting method 2: Patch the boot image yourself using the Magisk app on Android

- Copy the stock boot image file onto the Astro's storage
- Download and install the Magisk app on the Astro (be sure to only ever download it from the [official Magisk GitHub](https://github.com/topjohnwu/Magisk)). Get the full APK of the latest version from the [Releases page](https://github.com/topjohnwu/Magisk/releases), e.g. `Magisk-v26.1.apk`
- Open the Magisk app
- Tap 'Install' in the 'Magisk' card
- Tap 'Select and Patch a File'
- Browse to, and select, the stock boot image file
- Tap 'Let's Go', and wait ~15 seconds for the patching to complete
- Copy the file mentioned in the output onto your computer and rename it as `boot-magisk.img`
- Reboot to fastboot - run: `adb reboot fastboot`
- Flash the rooted boot image to the Astro - run: `fastboot flash boot boot-magisk.img`
- Reboot: `fastboot reboot`

### Rooting method 3: Patch the boot image yourself using a script

Note that the image file produced in this method has a different hash to the method above. With this method, you may encounter a stuck boot screen upon enabling Zygisk if you've accepted the prompt to let Magisk perform additional setup ([manually disable Zygisk to fix booting](https://github.com/shymega/planet-devices/wiki/Astro-troubleshooting#booting-stuck-after-enabling-zygisk-in-magisk)).

- Patch the image using [@shymega](https://github.com/shymega)'s scripts:
    + `wget https://github.com/shymega/magisk-boot-patch-ci-tool/archive/refs/tags/v1.3.0.zip`
    + `unzip v1.3.0.zip`
    + `magisk-boot-patch-ci-tool-1.3.0/patch.sh boot.img`
    + That'll download and use Magisk to patch it, writing the result as `root-boot.img`
- Reboot to fastboot - run: `adb reboot fastboot`
- Flash the rooted boot image to the Astro - run: `fastboot flash boot root-boot.img`
- Reboot: `fastboot reboot`
- Install the full Magisk app from the stub present in the app drawer, and hide root if necessary

## Unlocked bootloader warning/prompt

After rooting, a warning/prompt is added to the boot screen in tiny writing. You'll always have to press the power button within 5 seconds of the prompt to continue booting - unless you follow the instructions below to disable dm-verity.

The prompt reads:

> dm-verity corruption
>
> Your device is corrupt.  
> It can't be trusted and may not work properly.  
> Press power button to continue.  
> Or, device will power off in 5s.

The device will continuously boot loop this screen until you react.

Once you press the power button, the text changes to:

> Orange State
>
> Your device has been unlocked and cannot be trusted  
> Your device will boot in 5 seconds

### Remove dm-verity corruption prompt/warning

To remove this, disable dm-verity by flashing an empty vbmeta image:

- Back up vbmeta: `mtk r vbmeta_a vbmeta_a.img`
- Flash mtkclient's included empty vbmeta image: `mtk w vbmeta_a vbmeta.img.empty`

## Before applying an OTA update

An OTA update will expect the device to be in its stock state. You can remain unlocked and rooted, but partitions will likely need to be restored.

- Undo any changes you've made to the `system` partition (or avoid making them in the first place by instead making systemless changes using Magisk packages)
- Restore the boot image
- Restore the vbmeta image
- Apply the OTA update
- Again make your customisations to system/boot/vbmeta
