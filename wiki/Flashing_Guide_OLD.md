## <span style="color: #ff0000;">This Flashing guide is now marked as obsolete. </span>

<span style="color: #ff0000;"><span style="color: #000000;">Please use
the following pages to browse the updated current Flashing
guide:</span></span>

-   [Android Flashing Guide](Android_Flashing_Guide "wikilink")
-   [Linux Flashing Guide](Linux_Flashing_Guide "wikilink")

##  Introduction

This document will guide you through the necessary steps needed to flash
your Gemini with Linux or Android OS.

**Please note: <span style="color: #ff0000;">Flashing Android or Linux
will delete any user data on the device. Please make sure you have a
backup of any important data before starting!</span>**

<div style="text-align: justify;">

**Important Note: <span style="color: #ff0000;">please don’t use other
tools to install Linux on a Gemini as it’s easy to loose key information
such as IMEI. In particular, never use the “Format all + download“
option in the SP Flash Tool as this erases key information stored in the
NVRAM partition and can lead to a non-functional device.</span>**

</div>

## Download and Install FlashTool on Windows

 The first step is to install the flash tool drivers. These drivers are
needed for your Windows PC to communicate with your Gemini.

You can find the drivers here: [Windows Flash Tool
Drivers](http://support.planetcom.co.uk/download/Old/FlashToolDrivers.zip)

Once downloaded, unzip the archive. You will find a folder called
**FlashToolDrivers**, open the folder and double click on the
**Install** file. Allow the installation to complete by clicking Yes
when asked to make changes.

Now that the drivers have been installed, we can download the Windows
flash tool:  [Windows Flash
Tool](http://support.planetcom.co.uk/download/Old/FlashToolWindows.zip)

You will also need a firmware to flash, either Linux or Android. You can
find the available Gemini firmwares here: [Gemini Firmware
OLD](Gemini_Firmware_OLD "wikilink")

Once downloaded please unzip both the flash tool and the firmware. Next,
run the flash tool by double clicking on **flash_tool** in the
**FlashToolWindows** folder. Use the choose button as in the following
screenshot to load the scatter file that you will find inside the
downloaded firmware.

## Download and Install FlashTool on Linux

You can find the Linux flash tool software here: [Linux Flash
Tool](http://support.planetcom.co.uk/download/Old/FlashToolLinux.tgz)

You will need a 64 bit Linux machine and you might need root access to
run it. The executable file is flash_tool.sh.
<span style="caret-color: #2b2e2f; color: #2b2e2f; font-family: 'Lucida Sans Unicode', 'Lucida Grande', Tahoma, Verdana, sans-serif; font-size: 14px; font-style: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: auto; word-spacing: 0px; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; text-decoration: none; display: inline !important; float: none;">If
you get a BROM error when connecting the Gemini (see flash_tool console
log) then you should follow this guide
</span>[<https://forum.xda-developers.com/general/rooting-roms/tutorial-how-to-setup-spflashtoollinux-t3160802/page16>](https://forum.xda-developers.com/general/rooting-roms/tutorial-how-to-setup-spflashtoollinux-t3160802/page16)<span style="caret-color: #2b2e2f; color: #2b2e2f; font-family: 'Lucida Sans Unicode', 'Lucida Grande', Tahoma, Verdana, sans-serif; font-size: 14px; font-style: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: auto; word-spacing: 0px; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; text-decoration: none; display: inline !important; float: none;"> -
specifically the 2 points regarding udev rules.</span>

## Configuring Flash Tool

Use the choose button as in the following screenshot to load the scatter
file that you will find inside the downloaded firmware. In particular:

-   Downlad-Agent should be set to the file MTK_AllInOne_DA.bin, which
    is located in the FlashToolWindows or FlashToolLinux folder.
-   Scatter-loading file should be set to the specific scatter file of
    the firmware that you want to flash, which is located in the
    firmware folder

![<File:flash1.png>](flash1.png "File:flash1.png")

## Backup the NVRAM partition

Before flashing the device with a different firmware it is a good idea
to backup the current NVRAM partition. This partition stores key
information for your Gemini, including the IMEI number. If it gets lost
or damaged, your Gemini will not be able to take or receive calls.

The provided flash tool is already configured for your Gemini. To create
a backup of your NVRAM partition, just click on the **Readback** tab and
then on the **Add** button. A row will appear in the table as in the
following screenshot.

![<File:nvram.png>](nvram.png "File:nvram.png") 

Next, just click the **Read Back** button, connect your Gemini to your
PC and restart the Gemini. Once rebooted, the flash tool will detect the
phone and will write the NVRAM partition on a file on your hard disk
called NVRAM0. It’s a good idea to keep this file as a backup.

## Flashing the Gemini with an alternative firmware

Be sure to follow the previous step to store a copy of the NVRAM
partition as backup. Now, run the Flash tool software and click on the
**Download** tab. Next, locate the **Scatter-loading File** option and
click on the associated **choose** **button**, as highlighted in the
picture below:

  ![<File:flash1.png>](flash1.png "File:flash1.png")

Now, open the firmware folder from the firmware zip file you downloaded
and select the scatter file.Each firmware package contains 2 firmware
versions: **Gemini_Android.txt** can be used to flash a standard Android
system, while **Gemini_Android_Rooted.txt** can be used to install a
rooted Android version. You can also install a dual boot Android/Linux
firmware, please refer to the [Gemini
Firmware](Gemini_Firmware "wikilink") to learn how to generate the
scatter file.

Once you select the scatter file, the table should be populated as
below:

![<File:flash2.png>](flash2.png "File:flash2.png")

 Finally, change the **Download Only** drop down menu to**Firmware
Upgrade** and click on the **Download** button. Connect your Gemini and
restart it. . Once rebooted, the flash tool will detect the phone and it
will update the OS with the selected firmware.

## Notes on flashing firmwares

When switching between a standard Android to a dual boot Android/Linux
firmware, you will need to use the **Firmware Upgrade**mode because you
need to format the device. If you don't need to repartition the device,
you can use the **Download Only**mode and flash a single partition
without formatting. This is useful because you can update the Android
system partition without deleting your data (which is stored in the user
data partition), or you can update the boot.img and switching from an
Android system to a rooted one or viceversa.

## Linux dual boot notes

The dual boot mechanism works as follow:

-   **Dual boot Android-Linux firmware**
    -   Press Esc (On) for around one second to turn ON the unit and
        boot into Android. You should release the Esc (On) button before
        the screen turns ON, otherwise the unit will boot into recovery
        mode (see below).
    -   Press Esc (On) for around one second to turn ON the unit and at
        the same time press and hold the side button until the screen
        turns ON to boot into Linux. You should release the Esc (On)
        button before the screen turns ON, but you must keep the side
        button pressed until you see the turning ON. When the screen
        turns ON you can release the side button, and the unit will boot
        into Linux.
    -   Press Esc (On) and keep pressing the button until the screen
        turns ON to boot in recovery mode. At this stage the recovery
        mode is disabled and you will see a droid image with a red
        triangle and a "No command" text.