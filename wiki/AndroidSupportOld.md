## <span id="Linux_Installation_Notes." class="mw-headline">Android Installation Notes.</span>

The following steps will allow you to flash an original Android firmware
or a Linux dual boot firmware. At the moment the flash tool only
supports Windows.

**Please note: <span style="color: #ff0000;">Flashing Android or Linux
will delete any user data on the device. Please make sure you have a
backup of any important data before starting!</span>**

1.  Install Windows FlashTool
    [d](http://support.planetcom.co.uk/download/FlashToolDrivers.zip)r[ivers](http://support.planetcom.co.uk/download/FlashToolDrivers.zip).
    **Note: The drivers have been updated to improve compatibility with
    Windows 10.**
2.  Download the [Flashing
    tool](http://support.planetcom.co.uk/download/FlashTool.zip)
3.  Use it with one of the following firmware:
    -   [Android firmware
        v1.0](http://support.planetcom.co.uk/download/Gemini_Android_1_1_0.zip)
    -   [Dual boot Android - Debian linux - Technology
        preview](http://support.planetcom.co.uk/download/Gemini_Debian_TP.zip)

[Here you can find information about the flashing
process.](Flashing_Guide "wikilink")

Please note that Linux support is still under development at the moment,
and the Debian technology preview is mainly for people who wants to
experiment with it. We will provide updated firmwares in the next few
weeks, please stay tuned!

## Rooted Android

With Gemini you have the option to easily root your device. Please bear
in mind that rooting an Android device comes with associated risks, and
some application might not work correctly. You can search the Internet
for more information, we suggest that you proceed only if you know what
you are doing.

If you know what you are  doing and you want to continue, then follow
these steps:

1.  Download the [rooted boot
    image](http://support.planetcom.co.uk/download/boot-verified.img)
2.  Follow the Android installation notes above but before flashing the
    unit, overwrite the original boot-verified.img file in the
    **Gemini_Android_1_1_0** folder with the rooted boot image that you
    just downloaded
3.  Complete the flashing and your device will now be rooted. Install
    [Magisk Manager](https://magiskmanager.com) to complete the process.