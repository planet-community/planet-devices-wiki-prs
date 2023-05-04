This page is aimed at users that soft bricked their Cosmo Communicator
by corrupting the the boot or recovery partition, for example because of
improper use of TWRP.

First of all, if you can still boot into the original Recovery mode,
then restoring a full Android firmware is easy. You will need to prepare
an SD card following these instructions ([Cosmo Android Firmware Manual
Installation](Cosmo_Android_Firmware_Manual_Installation "wikilink"))
and then use the Recovery mode to install the Android firmware.

In case you can't boot into Recovery mode, there could still be a chance
of recovering the Android installation if you can boot into TWRP. The
procedure here is a bit more complicated:

-   As in the previous case, you will need to prepare an SD card
    following these instructions ([Cosmo Android Firmware Manual
    Installation](Cosmo_Android_Firmware_Manual_Installation "wikilink"))
-   In this case, please **make sure you use version v23.**
-   After that, download [this
    file](https://support.planetcom.co.uk/download/Cosmo_Installer_V23_TWRP.sh)
    and place it into the SD card under the **cosmo-customos-installer**
    folder
-   Put the SD card into your Cosmo Communicator and boot into TWRP.
    Your SD content should be available in folder /auto0-1.
-   Tap on "Advanced" and then "Terminal" to open the terminal
    application
-   Finally, type the following commands (using the on-screen keyboard):

`cd /auto0-1/cosmo-customos-installer`

`sh Cosmo_Installer_V23_TWRP.sh`

This should restore your Andriod firmware on your Cosmo Communicator.

If you can't boot into either Recovery mode or TWRP then you will most
likely have to send the device to us for repair.