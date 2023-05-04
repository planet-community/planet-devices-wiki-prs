#### Download and Install Rooted Android for Firmware v25 (latest)

The latest Android Firmware v25 requires an updated rooted Android
Firmware.

You can download the latest archive file at this URL:

-   [<http://support.planetcom.co.uk/download/rooted_android_v25.zip>](http://support.planetcom.co.uk/download/rooted_android_v25.zip)
    (MD5: 261bfe7633494174157716aa8c8b9578)

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

Once you select a custom OS you have to select where to install its boot
firmware.

Once you select the boot partition, the custom OS will be installed on
your Cosmo Communicator. A boot menu will then appear when you turn ON
the device, allowing you to choose what to start as in the following
picture.

![](46.jpg "46.jpg")

Using this method you will be able to install a custom OS such as Linux
on your device without the need for a laptop or a desktop computer. All
you need to do is to download the installer in a micro SD card and use
the recovery mode to start the installation.

#### Completing Rooted Android Firmware setup

After booting into the rooted Android partition, complete the
installation by tapping on the Magisk application icon. Once started,
Magist will ask to upgrade to full Magisk to finish the setup.

<figure>
<img src="Screenshot_20210322-105526.png"
title="Screenshot_20210322-105526.png" width="800" height="400"
alt="Screenshot_20210322-105526.png" />
<figcaption
aria-hidden="true">Screenshot_20210322-105526.png</figcaption>
</figure>

Tap OK to Download and Install. The phone will then reboot into Recovery
mode, from which you can exit by press and hold the ESC button. The
installation is now complete, you can now install a root checker
application to verify that the phone is rooted. Please note that the
firmware will be rooted only when selecting ROOTED_ANDROID boot when
starting the phone. If you select NORMAL boot, then the standard Android
will be started.