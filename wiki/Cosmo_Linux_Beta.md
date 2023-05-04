## Linux installation guide

**<span style="color: #ff0000;">PLEASE DON'T USE THESE INSTRUCTIONS IF
YOU ARE NOT PART OF THE LINUX BETA PROGRAM</span>**

The first step to install Linux on your Cosmo is to make sure you are
running the latest Android firmware, currently v19. You can check the
Android version by tapping Settings -\> System -\> Advanced -\> About
Phone and scrolling to the end of the page as in the following
screenshot.

![](36.jpg "36.jpg")

Next you will have to download the Linux firmware, which will need to be
installed into the microSD card on your Cosmo. Insert a microSD card on
your cosmo and make sure it is formatted as MS-DOS(FAT32).

You can find the download archive at this address: 
[<http://support.planetcom.co.uk/download/cosmo-customos-installer-beta.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-beta.zip)

Once you downloaded the zip archive you will have to extract its content
onto your microSD card:

1.  Open Files by Google and locate the ZIP archive
2.  Tap the file to reveal the cosmo-customos-installer folder
3.  Long tap on that folder, select Extract to... and finally select the
    microSD card as desitination. Your microSD card should now contain a
    folder named cosmo-customos-installer with several files inside it.

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

The main requirement when installing Linux is to reserve space for it.
In order to do this you will have to re-partition your device, which
will lead to the loss of all your data. Once you reserve some space for
Linux you can update Android or Linux independently, without loosing
your data again. To change the partition table of your Cosmo use the
option "Change the partition table of your COSMO", as in the picture
below.

![](Screenshot_2020-02-12_at_15.12.52.png "Screenshot_2020-02-12_at_15.12.52.png")

You will have 5 options to choose from:

1.  Reserve all space for Android
2.  Reserve 90GB for Android and 30GB for Linux
3.  Reserve 60GB for Android and 60GB for Linux
4.  Reserve 30GB for Android and 90 GB for Linux
5.  Reserve all space for Linux

![](Screenshot_2020-02-12_at_15.15.52.png "Screenshot_2020-02-12_at_15.15.52.png")

If you select to reserve some space for Linux, 4 additional partitions
will be created:

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

-   TWRP (Team Win Recovery Project)
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

## TWRP installation

Follow the installation steps above and just remember that TWRP can only
installed in the EMPTY_RECOVERY_BOOT_2 partition.

## Debian/KDE installation

Simply follow the installation steps above. The Debian/KDE installer
will automatically install the boot image into the selected partition
and it will also install the rootfs image into the Linux partition.

### Tips

-   The password for the 'gemini' user is 'gemini'
-   The default keyboard layout is English. To configure a different
    keyboard layout, make sure you have updated your Linux distribution:
    1.  <s>Remove _apt user from /etc/passwd (see point below in known
        issues) </s>(Not needed anymore)<s>
        </s>
    2.  become root by typing 'sudo bash' followed by the 'gemini'
        password
    3.  type 'apt-get update'
    4.  type 'apt-get upgrade'.


Aget that, click on the menu icon and select System Settings. Inside
System Settings select "Input Devices" and set the Keyboard Model under
Hardware to "Planet \| Planet Computers Cosmo Communicator" as in the
screenshot below. Tap the Apply button.

![](55.jpg "55.jpg")

Under layout you can now select your own Cosmo keyboard layout.

-   WIFI - To setup the WIFI connection tap on the WIFI icon on the
    bottom right, select the WIFI network you want to connect to and tap
    Connect.

![](26.jpg "26.jpg")

### Known bugs

-   apt-get does not work straight out of the box yet. A quick hack
    needed to run it is to edit the /etc/passwd file and remove the
    _apt user.

<!-- -->

-   English keyboard layout is supported out of the box. Additional
    keyboard layouts are also present, but some keys might not work. You
    can fix this by updating your system. To update your Linux:
    1.  <s>Remove _apt user from /etc/passwd as in the previous
        point</s> (this is not needed anymore)
    2.  become root by typing 'sudo bash' followed by the 'gemini'
        password
    3.  type 'apt-get update'
    4.  type 'apt-get upgrade'.
-   Opening/Closing the unit does not suspend/resume the unit at this
    time. You will have to manually shutdown the unit via software when
    you want to terminate your Linux session.

## Rooted Android installation

Install the Rooted Android image as per the installation above.
After booting the rooted Android partition, complete the installation by
downloading and running Magisk Manager
([<https://magiskmanager.com>](https://magiskmanager.com)). The Magisk
Manager interface should then be similar to the following screenshot
(notice the green OK icon, device IS rooted).

![](53.jpg "53.jpg")

If instead you run Magisk Manager from a normal Android boot (not
rooted), it will look like in the following screenshot. The red icon
shows that the device is NOT rooted.

![](50.jpg "50.jpg")