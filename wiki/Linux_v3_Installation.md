## Cosmo Linux installation

#### Existing Linux installations

Before installing Linux, make sure you have the latest Android Firmware
installed, currently v25.

If you plan to update your current Linux installation to the latest
version, please make sure that you manually install CoDi firmware v15
(**Requirement 2** - see below) and [follow this
link.](Manual_Update_Linux_v3 "wikilink")

The rest of this guide details how to perform a fresh Linux
installation.

#### New Linux Installations

Before starting the installation, please be sure that you are running
the latest Android firmware, currently **V25 (Requirement 1)**.

#### Requirement 1 - Latest Android firmware v25

You can check the Android version by tapping Settings -\> System -\>
Advanced -\> About Phone and scrolling to the end of the page (see Build
number detail, in the screenshot below).

![](24_43.jpg "24_43.jpg")

#### Requirement 2 - Codi firmware v15

Using the latest Android firmware version v25 the Cover Display
application will automatically install the latest Codi firmware v15. It
is therefore recommended to update the Android firmware and use the
Cover Display to install the latest Codi firmware.

For reference, you can find how to manually install Codi v15 using
Android v23 [here](Manual_Install_Codi_v15 "wikilink").

#### Download and Install Linux firmware v3 (latest)

Next, you will have to download the Linux firmware file, which will need
to be installed onto the microSD card on your Cosmo. Insert a microSD
card on your Cosmo and make sure it is formatted as MS-DOS(FAT32).

The Linux firmware is part of an archive that also contains TWRP and
rooted Android.

You can download the latest archive file at this URL:

-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v3.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v3.zip)
    (MD5: f6a765389913c790174d05dfdcb031d9)

Older versions:

-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v2.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v2.zip)
    (MD5: ba7f88924eb4254ac4c2aeb1c59ce6d6)
-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v1.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v1.zip)
    (MD5: 554e8ec1f1c57b0fc3a6140b1ecad3ea)

Alternatively, you can also purchase a Linux Media Installation Card
with the firmware already preloaded onto a micro SD card. This can be
purchased from
[<https://store.planetcom.co.uk/collections/media-books/>](https://store.planetcom.co.uk/collections/media-books)

Once you downloaded the zip archive you will have to extract its content
onto your microSD card:

1.  Using the Files app (do not use File Manager app) locate the ZIP
    archive
2.  Tap the archive file to reveal the cosmo-customos-installer folder
3.  Long tap on that folder, select Extract to... and finally select the
    root folder of the microSD card as destination.
4.  Complete the ZIP extraction process.
5.  Your microSD card should now contain a folder named
    cosmo-customos-installer with several files inside it.

Next, you will have to boot into recovery mode. To do that, simply turn
ON your Cosmo while keeping pressed the volume up button on the outside
cover. The volume up button is the one on the fingerprint sensor, which
points UP when the unit is open. The unit should boot into recovery mode
and you should be able to see the Android logo, but nothing else - as in
the following screenshot.

![](39.jpg "39.jpg")

At this point, keep the ESC key pressed (top left key on the keyboard)
and press the volume up button from the outside cover again, then
release both keys. This following menu will be displayed.

![](41.jpg "41.jpg")

<span style="color: #ff0000;">The main requirement when installing Linux
is to reserve space for it. In order to do this you will have to
re-partition your device, which will lead to the loss of all your
data.</span> Once you reserve some space for Linux you can update
Android or Linux independently, without loosing your data again. To
change the partition table of your Cosmo use the option "Change the
partition table of your COSMO", as in the picture below.

![](Screenshot_2020-02-12_at_15.12.52.png "Screenshot_2020-02-12_at_15.12.52.png")

You will have 5 options to choose from:

1.  Reserve all space for Android
2.  Reserve 90GB for Android and 30GB for Linux
3.  Reserve 60GB for Android and 60GB for Linux
4.  Reserve 30GB for Android and 90 GB for Linux
5.  Reserve all space for Linux

![](Screenshot_2020-02-12_at_15.15.52.png "Screenshot_2020-02-12_at_15.15.52.png")

Note that in recent firmwares you will also have the option to keep all
the storage for Android while allowing the installation of TWRP and
rooted Android, which is useful if you want to have a rooted Android
without using Linux.

If you select to install Linux, 4 additional partitions will be created:

1.  EMPTY_RECOVERY_BOOT_2 - This partition can be used to store an image
    that runs in recovery mode, such as TWRP
2.  EMPTY_NORMAL_BOOT_3 - This partition can be used to store Debian/KDE
    or Rooted Android
3.  EMPTY_NORMAL_BOOT_4 - This partition can be used to store Debian/KDE
    or Rooted Android
4.  In addition, an extra partition will be created with the custom size
    selected by the user, which will be used to store the root file
    system.

Once the storage for Linux has been reserved, you can install a custom
OS on your Cosmo, by choosing the related option as in the picture
below.

![](Screenshot_2020-02-12_at_15.18.42.png "Screenshot_2020-02-12_at_15.18.42.png")

This option will scan the microSD card for compatible installers and
will present you with a menu showing the available installers as in the
picture below.

![](43.jpg "43.jpg")

Whenever new or updated custom operating systems will be available for
the Cosmo, you will be able to download them into a micro SD card and
install it in your device.

At the moment we have initial support for the following:

-   TWRP (Team Win Recovery Project) **Please use caution when using
    TWRP as it can brick your device.TWRP support is limited for Cosmo
    Communicator (you can't access the encrypted user data partition)
    and its usage is discouraged. Use it at your own risk.**
-   Debian using KDE/Plasma - beta
-   Rooted Android

Once you select a custom OS you have to select where to install its boot
firmware. Remember that you can install TWRP only on the
EMPTY_RECOVERY_BOOT_2 partition, while you can install Debian/KDE and
the Rooted android image in either EMPTY_NORMAL_BOOT_3 or
EMPTY_NORMAL_BOOT_4 partitions.

Once you select the boot partition, the custom OS will be installed on
your Cosmo Communicator. A boot menu will then appear when you turn ON
the device, allowing you to choose what to start as in the following
picture.

![](46.jpg "46.jpg")

Using this method you will be able to install a custom OS such as Linux
on your device without the need for a laptop or a desktop computer. All
you need to do is to download the installer in a micro SD card and use
the recovery mode to start the installation.

You can watch a Cosmo Communicator How-To video detailing the Linux
installation process from SD card at this address
[<https://youtu.be/7guqI4nA8CU>](https://youtu.be/7guqI4nA8CU)