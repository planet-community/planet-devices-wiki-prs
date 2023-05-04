## Introduction

This document will guide you through the necessary steps needed to flash
your Gemini with a Linux or Android/Linux OS.

**Please note:** **<span style="color: #ff0000;">Flashing Android or
Linux will delete any user data on the device. Please make sure you have
a backup of any important data before starting!</span>**

<div style="text-align: justify;">

**Important Note: <span style="color: #ff0000;">please don’t use other
tools to flash firmware fo your Gemini as it’s easy to loose key
information such as the IMEI number. In particular, never use the
“Format all + download“ option in the SP Flash Tool as this erases key
information stored in the NVRAM partition and can lead to a
non-functional device.</span>**

</div>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>There
are 3 steps needed to install Android/Linux your Gemini:

</div>

1.  Install the FlashTool software on your Windows PC or Linux PC
2.  Customise your Gemini partition table. Using a simple tool, you will
    be able to specify the space you want to reserve for Linux and for
    Android. You will also be able to choose the firmware to download,
    at the moment we support Android, Rooted Android, Debian, Sailfish
    3.0 Beta Community Edition, Kali Linux and TWRP.
3.  Flash the firmware on your device

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>These
steps are detailed in the next sections.

</div>

## Download and Install FlashTool on Windows

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>The
first step to install FlashTool on a Windows PC is to install the flash
tool drivers. The drivers are needed for your Windows PC to communicate
with your Gemini, the minimum requirement is to have a 64bit Windows
operating system (Windows 7 or later supported).

</div>

You can find the latest drivers here: [Windows Flash Tool
Drivers](http://support.planetcom.co.uk/download/FlashToolDrivers.zip)

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>Once
downloaded, unzip the archive. You will find a folder
called **FlashToolDrivers**, open the folder and double click on
the **Install** (install.bat) file. Allow the installation to complete
by clicking **Yes** when asked to make changes.

</div>

Now that the drivers have been installed, you can download the latest
Windows flash tool: [Windows Flash
Tool](http://support.planetcom.co.uk/download/FlashToolWindows.zip)

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>Once
downloaded the Windows FlashTool, please unzip it to reveal
the **FlashToolWindows** folder. Next, run the flash tool by double
clicking on **flash_tool** (flash_tool.exe) file in
the **FlashToolWindows** folder.

</div>

## Download and Install FlashTool on Linux

**The following procedure has been tested on Debian 9.0, Ubuntu 18.04
(see notes below) and Fedora 28 (see notes below).**

You can find the latest Linux flash tool software here: [Linux Flash
Tool](http://support.planetcom.co.uk/download/FlashToolLinux.tgz)

Once downloaded, extract the flash tool by typing:

`tar -zxvf FlashToolLinux.tgz`

Before running the flash tool you will need to add some rules to udev.

Create the blacklist file by typing (using either the "sudo command" or
syntax or simply typing the command as root) :

`sudo gedit /etc/udev/rules.d/20-mm-blacklist-mtk.rules`

And inside the file put the following 2 lines:

`ATTRS{idVendor}=="0e8d", ENV{ID_MM_DEVICE_IGNORE}="1"`
`ATTRS{idVendor}=="6000", ENV{ID_MM_DEVICE_IGNORE}="1"`

After that, restart the udev:

`sudo service udev restart`

Finally, run the flash tool application by entering into the
**FlashToolLinux** folder and typing:

`cd FlashToolLinux`

`sudo ./flash_tool.sh`

**Notes - Ubuntu 18.04**

On Ubuntu you will need to install the following dependency:

`sudo apt-get install libjpeg62`

**Notes - Fedora 28**

On Fedora you will have to write the following command to allow
applications running with root privileges to access the X server (this
will fix the lines above for both gedit and flash_tool):

`xhost +local:`

Additionally you will have to restart the udev service by typing (or
rebooting your machine):

`udevadm control --reload-rules && udevadm trigger`

Finally, you will need to install the following dependency:

`sudo dnf install nas-libs-1.9.4-13.fc28.x86_64`

**Building the flash tool from source**

You can also build the flash tool by yourself, the code is hosted on
github: [Flash Tool
Source](https://github.com/dguidipc/SP-Flash-Tool-src)

## Customise your Gemini partition table

If you choose to flash a Linux or Android-Linux firmware, then you will
have to repartition your device, reserving some space for Linux and some
for Android. To repartition your Gemini you will have to use our
partition tool, available at
[<http://support.planetcom.co.uk/partitionTool.html>](http://support.planetcom.co.uk/partitionTool.html).
A screenshot of the tool is provided below.

![](Screen_Shot_2018-06-20_at_11.06.06.png "Screen_Shot_2018-06-20_at_11.06.06.png")

You can choose the partition size for Linux and Android by dragging the
planet slider left or right. You can choose to have an Android-only
Gemini, a multi boot Linux-Android or a Linux-only Gemini. Once you have
selected the partition sizes you have to select your Gemini model using
the appropriate drop down menu.

There are 3 Gemini versions, please make sure you select the right
version for your device:

-   WiFi-Only Gemini users should select "Gemini WIFI-Only".
-   4G Gemini users using x25 chip (early release Geminis) should select
    "Gemini x25"
-   Gemini 4G x27 users should select the "Gemini x27" option.

If you are not sure about your Gemini version, just check under Settings
-\> Wireless & networks. If you see a menu called SIM cards, then you
have an x27 Gemini, otherwise you have an x25 Gemini.

After selecting the partition size, you can select the operating systems
to use for each boot mode. Gemini supports 4 boot modes (see the Linux
boot notes section below for more information):

-   Boot 1: This is the default booting option when no buttons are
    pressed.
-   Recovery Mode: Esc (On) is pressed. This will always boot into overy
    mode.
-   Boot 2: Side button is pressed.
-   Boot 3: Esc(On) key is pressed and Side button is also pressed

As an example, the following screenshot shows a Gemini WIFI-Only model,
configured with 28 GB for both Android and Linux, where the boot modes
are set as:

-   Boot 1: Standard Android
-   Boot 2: Debian GNU/Linux
-   Boot 3: Sailfish OS

![](Screen_Shot_2018-06-20_at_11.16.03.png "Screen_Shot_2018-06-20_at_11.16.03.png")

After you made your selection, there are 3 modules to download using the
buttons on the right:

-   The**Base firmware** contains the basic Android firmware. This is
    the main component, it needs to be extracted to reveal the Gemini
    Base firmware folder. All the other component need to be
    copied/unzipped here.
-   The **Scatter file** contains the definition of your Gemini
    partition, based on your selection. This needs to be copied into the
    firmware folder
-   The optional **Linux module** (Debian, Sailfish 3.0 Beta for Gemini
    Community Edition, or Kali Linux) contains the additional Linux
    firmware. This needs to be unzipped inside the firmware folder

You should end up with the extracted Base firmware folder, containing
also the scatter file and the unzipped optional Linux module.

<span style="color: #ff0000;">**NOTE:**<span style="color: #000000;">**It
is important to keep a backup of the custom scatter file that you
created,**</span></span><span style="color: #ff0000;"><span style="color: #000000;">**you
will need it each time you want to update your device (for example
Android) without loosing your data.**</span></span>

##  Configuring Flash Tool

Use the choose button as in the following screenshot to load the scatter
file that you will find inside the downloaded firmware. In particular:

-   Download-Agent should be set to the file MTK_AllInOne_DA.bin, which
    is located in the FlashToolWindows or FlashToolLinux folder.
-   Scatter-loading file should be set to the specific scatter file of
    the firmware that you customised, which is located in the firmware
    folder

Your screen should look like the following screenshot:

![](Screen_Shot_2018-06-21_at_11.35.58.png "Screen_Shot_2018-06-21_at_11.35.58.png")

In particular, all the partitions should be checked. If you see any
unchecked partitions in the list, make sure you unzipped the Linux
module in the firmware folder and try again.

## Backup the NVRAM partition

Before flashing the device with a different firmware it is a good idea
to backup the current NVRAM partition. This partition stores key
information for your Gemini, including the IMEI number. If it gets lost
or damaged, your Gemini will not be able to take or receive calls.

The provided flash tool is already configured for your Gemini. To create
a backup of your NVRAM partition, just click on the **Readback** tab and
then on the **Add** button. A row will appear in the table as in the
following screenshot.

![](Screen_Shot_2018-06-21_at_10.52.02.png "Screen_Shot_2018-06-21_at_10.52.02.png")

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">Next,
just click
the </span><strong style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial;">Read
Back</strong><span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;"> button,
connect your PC to the left end USB-C port on your Gemini and restart
the Gemini. Once booted, the flash tool will detect the unit and will
write the NVRAM partition on a file on your hard disk called NVRAM0 (see
screenshot below). It’s a good idea to keep this file as a backup,
together with the customised Scatter file.</span>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;"><img src="Screen_Shot_2018-06-21_at_10.51.50.png"
title="Screen_Shot_2018-06-21_at_10.51.50.png" width="800" height="527"
alt="Screen_Shot_2018-06-21_at_10.51.50.png" /></span>

## Flashing the Gemini Linux firmware

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>Be sure
to follow the previous step to store a copy of the NVRAM partition as
backup.Now click back on the **Download** tab.

</div>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>Select
the **Firmware Upgrade** option from the drop down menu. This will
automatically select all the partitions in the table.

</div>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">To
start the flashing process, just click the
big </span><strong style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial;">Download</strong><span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;"> button,
connect your PC to the left end USB-C port on your Gemini and restart
the Gemini. Once booting, the flash tool will detect the unit and will
start flashing the device with the selected firmware.</span>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">The
following screenshot shows a successfully completed flashing
process:</span>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">![](Screen_Shot_2018-06-21_at_12.08.02.png "Screen_Shot_2018-06-21_at_12.08.02.png")</span>

## Troubleshooting

We made efforts to make sure that the flash procedure is fail-safe, but
sometimes background processes or other causes might interfere with the
process. If this happens, you might experience an error such as "Failed
to get PMT info", "Invalid ROM or PMT address" or
"STATUS_DOWNLOAD_EXCEPTION".

If you experience this issue, please follow the actions below:

1.  Disconnect your Gemini from your PC
2.  Press and hold the Esc (On) key and the silver side button until the
    unit restarts (until the unit vibrate)
3.  Reboot your PC
4.  Try the flash process again, it should now complete without issues

## Rooted Android notes

If you choose to flash the rooted Android firmware, remember that you
will have to complete the process by installing [Magisk
Manager](https://magiskmanager.com/) using the following steps.

1.  Allow the installation of unknown applications
    ![](Screenshot_20190212-124142.png "Screenshot_20190212-124142.png")

2.  Navigate to <https://magiskmanager.com>
    ![](Screenshot_20190212-123531.png "Screenshot_20190212-123531.png")

3.  Scroll down to 'Download Magisk Manager'. Click on the download
    button and install the application.
    ![](Screenshot_20190212-123546.png "Screenshot_20190212-123546.png")

4.  Open the application. If you arre running the app in a non-rooted
    Android you will see the error 'Magisk is not installed'.
    ![](Screenshot_20190212-123732.png "Screenshot_20190212-123732.png")

5.  When asked about Additional Setup, Tap on Yes and let the process
    complete.
    ![](Screenshot_20190212-123822.png "Screenshot_20190212-123822.png")

6.  Congratulations, you are running rooted Android on your Gemini!
    ![](Screenshot_20190212-123849.png "Screenshot_20190212-123849.png")

##  Linux boot notes

The multi-boot mechanism works as follows.

Starting from a switched OFF Gemini, press the Esc (On) key to start the
unit until the Gemini vibrates. Once you feel the vibration you can
choose the boot mode by pressing the following key combination:

-   Boot 1: This is the default booting option when no keys or buttons
    are pressed.
-   Recovery Mode: Esc (On) is pressed. This will always boot into
    recovery mode.
-   Boot 2: silver right-end side button is pressed.
-   Boot 3: Both Esc(On) key and silver right-end side button are
    pressed at the same time

Keep the keys/buttons pressed until the screen turns ON.