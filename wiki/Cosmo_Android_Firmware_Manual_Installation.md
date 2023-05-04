Follow this guide to manually install a specific Android version for
your Cosmo Communicator.

You can download the available Android firmware archive below:

-   [<http://support.planetcom.co.uk/download/cosmo-android-v23.zip>](http://support.planetcom.co.uk/download/cosmo-android-v23.zip)
    (MD5: 1f1f85cec23aa307e1ff980ad014d415)
-   [<http://support.planetcom.co.uk/download/cosmo-android-v22.zip>](http://support.planetcom.co.uk/download/cosmo-android-v22.zip)
    (MD5: 63ff496aa47dd72fc81fdc3d3be2a1cb)
-   [<http://support.planetcom.co.uk/download/cosmo-android-v19.zip>](http://support.planetcom.co.uk/download/cosmo-android-v19.zip)
    (MD5: 4cfe693455042b4479e6638ba005f3d3)

Please note that if you perform an upgrade, then  your user data will be
preserved. However, if you downgrade this is not always the case. For
example, when downgrading from v22 to v19 the device will not be able to
access your data because of the downgraded security patches, and it will
prompt you for a factory reset.

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

To be able to install a specific Android version you first need to
partition your device to accept custom OS. In order to do this you will
have to re-partition your device, which will lead to the loss of all
your data. If you already have partition your device you don't need to
do it again.

To change the partition table of your Cosmo use the option "Change the
partition table of your COSMO", as in the picture below.

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

This option will scan the microSD card for compatible installers and it
should find one or more, for example:

-   Reinstall Android V19 (Factory Reset)

Select the appropriate OS and press the Enter key. If you see a screen
asking to select where to install the custom OS (for example in
EMPTY_RECOVERY_BOOT_2, EMPTY_NORMAL_BOOT_3 or EMPTY_NORMAL_BOOT_4), just
select any available option and press Enter again. The Android firmware
will overwrite the standard Android and will not affect any other custom
OS that you might have installed.

After the installation is completed, reboot the unit. A boot menu will
then appear when you turn ON the device, allowing you to choose what to
start as in the following picture.

![](46.jpg "46.jpg")

After the Android firmware installation you can repartition your Cosmo
to only store Android and regain the space reserved for Linux, if you
want to.