## Introduction

This document will guide you through the necessary steps needed to
install or update Android on your Gemini.

**Please note: ** **<span style="color: #ff0000;">Installing Android
will delete any user data on the device. Please make sure you have a
backup of any important data before starting!</span>**

<div style="text-align: justify;">

**Important Note: <span style="color: #ff0000;">Please don’t use other
tools to flash firmware fo your Gemini as it’s easy to loose key
information such as the IMEI number. In particular, never use the
“Format all + download“ option in the SP Flash Tool as this erases key
information stored in the NVRAM partition and can lead to a
non-functional device.

</span>**

</div>

There are 3 steps needed to install or upgrade Android on your Gemini:

1.  Install the FlashTool software on your Windows PC or Linux PC
2.  Download and unzip the Android firmware
3.  Flash the firmware on your device

These steps are detailed in the next sections.

##  Download and Install FlashTool on Windows

The first step to install FlashTool on a Windows PC is to install the
flash tool drivers. The drivers are needed for your Windows PC to
communicate with your Gemini, the minimum requirement is to have a 64bit
Windows operating system.

You can find the latest drivers here: [Windows Flash Tool
Drivers](http://support.planetcom.co.uk/download/FlashToolDrivers.zip)

Once downloaded, unzip the archive. You will find a folder called
**FlashToolDrivers**, open the folder and double click on the
**Install** (install.bat) file. Allow the installation to complete by
clicking **Yes** when asked to make changes.

Now that the drivers have been installed, you can download the latest
Windows flash tool: [Windows Flash
Tool](http://support.planetcom.co.uk/download/FlashToolWindows.zip)

Once downloaded the Windows FlashTool, please unzip it to reveal the
**FlashToolWindows** folder. Next, run the flash tool by double clicking
on **flash_tool** (flash_tool.exe) file in the **FlashToolWindows**
folder.

## Download and Install FlashTool on Linux

If you intend to install FlashTool on a Windows PC you can skip this
section, otherwise please keep reading if you want to install FlashTool
on a Linux PC.

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
will fix the lines above for both the gedit and the flash_tool command):

`xhost +local:`

Additionally you will have to  restart the udev service by typing (or
rebooting your machine):

`udevadm control --reload-rules && udevadm trigger`

Finally, you will need to install the following dependency:

`sudo yum install nas-libs-1.9.4-13.fc28.x86_64`

**Building the flash tool from source**

You can also build the flash tool by yourself, the code is hosted on
github: [Flash Tool
Source](https://github.com/dguidipc/SP-Flash-Tool-src)

## Download Android Gemini Firmware

Now that the FlashTool application is running, it is time to download
the Gemini Android Firmware from the [Gemini Firmware
page](Gemini_Firmware "wikilink").

After downloading the firmware, unzip it to reveal the folder containing
the firmware folder, for example **Gemini_WIFI_MP_09052018** or
**Gemini_x27_FOTA3_12062018**.

## Configuring FlashTool

Use the choose button as in the following screenshot to load the scatter
file that you will find inside the downloaded firmware. In particular:

-   Downlad-Agent should be set to the file MTK_AllInOne_DA.bin, which
    is located in the FlashToolWindows or FlashToolLinux folder.
-   Scatter-loading file should be set to the **Gemini_Android.txt**
    file, which is located inside the of the firmware folder that you
    downloaded.

![](Screen_Shot_2018-06-21_at_10.45.58.png "Screen_Shot_2018-06-21_at_10.45.58.png")

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

Next, just click the **Read Back** button,
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">connect
your PC to the left end USB-C port on your Gemini</span> and restart the
Gemini. Once booting, the flash tool will detect the unit and will write
the NVRAM partition on a file on your hard disk called NVRAM0 (see
screenshot below). It’s a good idea to keep this file as a backup.

![](Screen_Shot_2018-06-21_at_10.51.50.png "Screen_Shot_2018-06-21_at_10.51.50.png")

## Flashing the Gemini Android firmware

Be sure to follow the previous step to store a copy of the NVRAM
partition as backup.Now click back on the **Download** tab.

If you want to flash the complete firmware to your unit then select
**Firmware Upgrade** from the drop down menu.This will automatically
select all the partitions in the table and it will restore your unit to
its factory state. Please note that you will loose all your personal
data/settings. 

Your screen should appear similar to the following screenshot:

![](Screen_Shot_2018-06-21_at_11.01.20.png "Screen_Shot_2018-06-21_at_11.01.20.png")

To start the flashing process, just click the big **Download** button,
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">connect
your PC to the left end USB-C port on your Gemini</span> and restart the
Gemini. Once booting, the flash tool will detect the unit and will start
flashing the device with the selected firmware.

If instead you want to manually update your Gemini without loosing your
data, you should select the **Download Only**option from the drop down
menu. After that, make sure you select all the partition with the
exception of the **userdata** partition, which contains your data. Your
screen should look like this:

![](Screen_Shot_2018-06-21_at_11.12.29.png "Screen_Shot_2018-06-21_at_11.12.29.png")

To start the flashing process, just click the big **Download** button,
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">connect
your PC to the left end USB-C port on your Gemini</span> and restart the
Gemini. Once booting, the flash tool will detect the unit and will start
flashing the device with the selected firmware.

The following screenshot shows a successfully completed flashing
process:

![](Screen_Shot_2018-06-21_at_11.17.44.png "Screen_Shot_2018-06-21_at_11.17.44.png")