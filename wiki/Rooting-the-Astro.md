Rooting: the Astro Slide (manual)
=================================

To (manually) root the Astro Slide, you can use this guide:

You will need:

- Astro Slide 5G (obviously).
- A machine running Linux. (I did this with Linux Mint, but I expect this'll work on most flavours.) It'll need to be a fairly recent version, to satisfy the mtk requirements.
- USB cable to connect the Astro (USB-C) to the Linux machine.

Procedure:
1. If you've used the Astro already, take a backup of anything you want to keep (apps, data, settings, etc.) as this will wipe it to factory settings.
2. *Unlock* the bootloader, so that the root image can boot. The Astro will
   soft-brick if you use unsigned boot images. You can do this by using Fastboot
   and the `OEM Unlocking` in Settings -> Developer Options.
3. Install mtkclient on the Linux box, following all the Linux instructions here.
4. Extract the boot image from the Astro:
    - Shut down the Astro.
    - Connect the Linux box to the Astro's bottom/right USB port.
    - `mtk r boot_a boot.img`
    - Wait for that to finish, then disconnect.
    - That'll save the image to the file boot.img.
5. Patch the image using Dom's scripts here:
    - `wget https://github.com/shymega/magisk-boot-patch-ci-tool/archive/refs/tags/v1.2.0.zip`
    - `unzip v1.2.0.zip`
    - `magisk-boot-patch-ci-tool-1.2.0/patch.sh boot.img`
    - That'll download and use Magisk to patch it, writing the result as root-boot.img.
6. Write the patched image back to the Astro:
    - Make sure the Astro is still powered off.
    - Connect the Linux box to the Astro's bottom/right USB port.
    - `mtk w boot_a root-boot.img`
    - Wait for that to finish, then disconnect.
7. Boot the Astro back up.
8. Install the full Magisk app in the stub app present in the app drawer, and hide root if necessary.
