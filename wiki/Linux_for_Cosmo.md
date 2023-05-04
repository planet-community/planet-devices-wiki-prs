## Linux News

**28/04/2021 - The latest Linux Debian firmware v4 is now available!**

<span style="color: #ff0000;">Please note we are investigating an issue
related to not receiving incoming calls with this version of
Linux.</span>

Thanks to the ongoing support from the open source community, today we
are glad to release the latest Linux Debian v4 for Cosmo Communicator!

This latest release provides bug fixes and new features:

-   Support for Camera is now available
-   Improved boot screen and lock  screen
-   Support for dual keyboard language layout. If you use a dual
    keybaord layout, such as Japanese, you can press both shift keys at
    the same time to cycle between the layouts (i.e. english and
    japanese).
-   New installation program allows you to select your keyboard layout
    and time zone. The information is then stored in phone settings and
    retained even after Linux reinstallation.

Please note that altough it's possible to keep using Linux v3, updating
from v3 to v4 using apt is not possible.

**It's therefore recommended to use the guide below to install Linux
v4.**

Notes on Linux v4 installation:

-   The new installer will allow you to select your keyboard layout and
    time zone
-   If you use a dual keyboard layoyut, your settings might not be
    picked up on the very first boot. For example if you choose Japanese
    layout, on your first boot the screen and keyboard layout could
    still be set to English. Simply reboot the unit and both the
    language and keyboard layout will be fully configured. Remember you
    can switch between the 2 keyboard layouts by pressing both left and
    right shift buttons at the same time.

For more information about this release, please see
[here](https://gemian.thinkglobally.org/releases/2021-04-22-gemian-release-notes.txt).

**11/12/2020 - Linux update
**

Today we released a new update for Linux users! It can be installed by
typing the following commands in a terminal:

`sudo apt update`

`sudo apt upgrade`

Please reboot the unit after these commands.

The update includes a brand new feature which allow users to set the
keyboard brightness either by using the key combinations Shift+Fn+B and
Shift+Fn+N or by setting its value in the settings (System Settings
-\>Power Management -\> Energy Saving -\> Keyboard backlight)

The update also contains keyboard improvements and CoDi bug fixes.

**18/11/2020 - The latest Linux Debian firmware v3 is now available!**

This release contains a Cover Display (CoDi) implementation for Linux
which provides a number of new features, such as:

-   Mouse Control - you can now use the CoDi display as a trackpad when
    the unit is open
-   Phone Control - you can browse contact and place/accept calls from
    the Codi screen while the unit is closed
-   Device Control - you can switch OFF/reboot Cosmo from the CoDi
    display
-   Contacts can be updated by the gka-contacts-qt application or
    directly from the dialer app


A big thank you to the Cosmo Communicator open source community for
supporting Linux on Cosmo Communicator!

![](Screenshot_20201118_110844.png "Screenshot_20201118_110844.png")

![](Screenshot_20201118_111109.png "Screenshot_20201118_111109.png")

To see some of the new features, please take a look at this Cosmo
Communicator update video
[<https://youtu.be/aljMVuzT5-Y>](https://youtu.be/aljMVuzT5-Y)

Older Linux Debian v2 firmware

The Linux Debian v2 firmware has numerous bug fixes and supports the
following new features:

-   Phone Calls
-   SMS support
-   4G Mobile data support using connman
-   Open/Close power save support

## Cosmo Linux installation

Before installing Linux, make sure you have the latest Android Firmware
installed, currently v25.

Touchpad functionality for Linux is added in the latest CoDi, version
1.1.1.16.

#### Download and Install Linux firmware v4 (latest)

You will have to download the Linux firmware file, which will need to be
installed onto the microSD card on your Cosmo. Insert a microSD card on
your Cosmo and make sure it is formatted as MS-DOS(FAT32).

You can download the latest archive file at this URL:

-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v4.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v4.zip)
    (MD5: 8e5b2ec60d45627e66828f419fe63199)

Older versions:

-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v3.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v3.zip)
    (MD5: f6a765389913c790174d05dfdcb031d9)
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

## TWRP installation

**Please use caution when using TWRP as it can brick your device.**

**TWRP support is limited for Cosmo Communicator (you can't access the
encrypted user data partition) and its usage is discouraged.**

**Use it at your own risk.**

Follow the installation steps above and just remember that TWRP can only
installed in the EMPTY_RECOVERY_BOOT_2 partition.

## Debian/KDE installation

Simply follow the installation steps above. The Debian/KDE installer
will automatically install the boot image into the selected partition
and it will also install the rootfs image into the Linux partition.

**The latest Linux v4 will automatically configure the keyboard layout
based on the installation choice. The following guide is obsolete and
kept as reference.**

#### Keyboard Layout Configuration

The default keyboard layout is American English, to configure a
different layout, see the example command below.

The following command can be used to set the keyboard layout to English
(GB):

`setxkbmap -model planetcosmo -layout gb`

To restore the layout to English (US), use the following command:

`setxkbmap -model planetcosmo -layout us`

#### WIFI Configuration

To setup the WIFI connection tap on the NetworkManager icon on the
bottom right, select the WIFI network you want to connect to and tap
Connect.

![](10.jpg "10.jpg")

After entering the password, the system will ask you how to store the
password. If you want to store it without entering a password, then
select the first option "Classic, blowfish encrypted file" and when
asked to enter a password just leave it empty and tap OK. The system
will then popup a warning that the password has a low strength, just tap
on the Yes button.

![](21.jpg "21.jpg")

### Phone and Message apps

The latest Linux update comes with a phone dialler and an SMS message
app. They are available under the Phone application category

![](23_33.jpg "23_33.jpg")

Both applications are quite simple and work as expected. Both apps have
a special button at the botton that can be swiped up to reveal more
information. For example the Phone Dialler app will show recent and
missed calls as in the picture below.

![](23_28.jpg "23_28.jpg")

### Enbling Mobile Data

Please note that WIFI, Phone calls and SMS work straight away.

The default NetworkManager application also supports mobile data, but it
does not work well with Cosmo.

To activate mobile data [please follow this
link](Mobile_Data_In_Linux_Cosmo "wikilink").

### Tips

-   There is a default user named 'cosmo'. The password for the 'cosmo'
    user is 'cosmo'
-   To update your Linux installation, make sure you configure a WIFI
    connection and then:
    1.  Become root by typing 'sudo bash' followed by the 'cosmo'
        password
    2.  type 'apt update'
    3.  type 'apt upgrade'.
-   On Linux, the ESC key sends the Escape command on Linux. To send the
    power command, use Fn+ESC.

## Rooted Android installation

**Please see [this page for instruction on how to install Rooted Android
on a Cosmo.](Rooted_Android_For_Cosmo "wikilink")**

The following information is now outdated and kept as reference only.

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