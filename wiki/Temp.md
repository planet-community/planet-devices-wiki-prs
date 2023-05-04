## Linux News

The latest Linux Debian firmware is now available!

The latest Linux firmware has numerous bug fixes and supports the
following new features:

-   Phone Calls
-   SMS support
-   4G Mobile data support using connman
-   Open/Close power save support

Many thanks for the Cosmo Communicator open source community for
supporting Linux on Cosmo Communicator!

## Linux installation

The first step to install Linux on your Cosmo is to make sure that you
are running the latest Android firmware, currently **V23**. You can
check the Android version by tapping Settings -\> System -\> Advanced
-\> About Phone and scrolling to the end of the page (see Build number
detail, in the screenshot below).

![](24_43.jpg "24_43.jpg")

Next you will have to download the Linux firmware, which will need to be
installed into the microSD card on your Cosmo. Insert a microSD card on
your Cosmo and make sure it is formatted as MS-DOS(FAT32).

The Linux firmware is part of an archive that also contains TWRP and
rooted Android.

You can download the latest archive at this URL:

-   [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v2.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v2.zip)
    (MD5: ba7f88924eb4254ac4c2aeb1c59ce6d6)
-   The older v1 version is available here:
    [<http://support.planetcom.co.uk/download/cosmo-customos-installer-v1.zip>](http://support.planetcom.co.uk/download/cosmo-customos-installer-v1.zip)
    (MD5: 554e8ec1f1c57b0fc3a6140b1ecad3ea)

Alternatively, you can also purchase a Linux Media Installation Card
with the firmware already preloaded onto the micro SD card. This can be
purchased from
[<https://store.planetcom.co.uk/collections/media-books/>](https://store.planetcom.co.uk/collections/media-books)

Once you downloaded the zip archive you will have to extract its content
onto your microSD card:

1.  Open Files by Google and locate the ZIP archive
2.  Tap the file to reveal the cosmo-customos-installer folder
3.  Long tap on that folder, select Extract to... and finally select the
    microSD card as destination. Your microSD card should now contain a
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

#### Keyboard Layout Configuration

The default keyboard layout is American English. To configure a
different keyboard layout, click on the menu icon and select System
Settings. Inside System Settings select "Input Devices" and set the
Keyboard Model under Hardware to "Planet \| Planet Computers Cosmo
Communicator" as in the screenshot below. **Tap the Apply button**.

![](55.jpg "55.jpg")

Next, go to the Layouts tab where you can select your own Cosmo keyboard
layout. For example, to select the British UK keyboard layout, tap on
"Configure layouts" and specify the English (GB) keyboard layout, as in
the following screenshot.

![](23_04.jpg "23_04.jpg")

You can also use command line to set the keyboard hardware model and
layout. The following command can be used to set the keyboard layout to
English (GB):

`setxkbmap -model planetgemini -layout gb`

To restore the layout to English (US), use the following command:

`setxkbmap -model planetgemini -layout us`

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