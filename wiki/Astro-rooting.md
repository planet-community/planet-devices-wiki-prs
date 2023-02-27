# Rooting: the Astro Slide (manual)

To (manually) root the Astro Slide, you can use this guide:

## Requirements

- An **Astro Slide 5G** (obviously).
- **A machine running Linux**. (I did this with Linux Mint, but I expect this'll work on most flavours.) It'll need to be a fairly recent version, to satisfy the `mtkclient` [requirements](https://github.com/bkerler/mtkclient/blob/main/requirements.txt).
- **USB cable** to connect the Astro (USB-C) to the Linux machine.

## Procedure

1. If you've used the Astro already, **take a backup** of anything you want to keep (apps, data, settings, etc.) as this will wipe it to factory settings.
2. **Unlock** the bootloader, so that the root image can boot. The Astro will
   soft-brick if you use unsigned boot images. You can do this by following [this](https://www.ifixit.com/Guide/How+to+unlock+the+bootloader+of+an+Android+Phone/152629) guide here.
3. **Install [mtkclient v1.52](https://github.com/bkerler/mtkclient/archive/refs/tags/1.52.zip)** on the Linux box, following all the Linux instructions [here](https://github.com/bkerler/mtkclient).
4. **Extract the boot image** from the Astro:
    - **Shut down** the Astro.
    - Connect the Linux box to the Astro's bottom/right USB port.
    - `mtk r boot_a boot.img`
    - Wait for that to finish, then disconnect.
    - That'll save the image to the file boot.img.
5. **Patch the image** using [@shymega](https://github.com/shymega)'s scripts here:
    - `wget https://github.com/shymega/magisk-boot-patch-ci-tool/archive/refs/tags/v1.3.0.zip`
    - `unzip v1.3.0.zip`
    - `magisk-boot-patch-ci-tool-1.3.0/patch.sh boot.img`
    - That'll download and use Magisk to patch it, writing the result as root-boot.img.
6. **Write the patched image** back to the Astro:
    - Make sure the Astro is **still powered off**.
    - Connect the Linux box to the Astro's bottom/right USB port.
    - `mtk w boot_a root-boot.img`
    - Wait for that to finish, then disconnect.
7. **Boot the Astro** back up.
8. **Install the full Magisk app** from the stub present in the app drawer, and hide root if necessary.

## Unlocked bootloader warning/prompt

After rooting, a warning/prompt is added to the boot screen in tiny writing. You'll always have to press the power button within 5 seconds of the prompt to continue booting.

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
