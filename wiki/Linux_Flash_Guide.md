## Introduction

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

## Download and install flash tool drivers

 The first step is to install the flash tool drivers. These drivers are
needed for your PC to communicate with your Gemini. At the moment the
drivers are only available for Windows, they are also known to work
inside a Windows virtual machine running on a different operating
system.

You can find the drivers here:
[<http://support.planetcom.co.uk/index.php/Linux_Support>](http://support.planetcom.co.uk/index.php/Linux_Support)

Once downloaded, unzip the archive. You will find a folder called
**FlashToolDrivers**, open the folder and double click on the
**Install** file. Allow the installation to complete by clicking Yes
when asked to make changes.

## Download and install flash tool

Now that the drivers have been installed, we can download the flash
tool. You will also need a firmware to flash, either Linux or Android.
You can find the flash tool, alongside with the current available Linux
versions here:
[<http://support.planetcom.co.uk/index.php/Linux_Support>](http://support.planetcom.co.uk/index.php/Linux_Support)

Once downloaded please unzip both the flash tool and the firmware. Next,
run the flash tool by double clicking on **flash_tool** in the
**FlashTool** folder. The software will initially complain that he
cannot find the scatter file.  Use the choose button as in the following
screenshot to load the scatter file that you will find inside the
downloaded firmware.

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
and select the scatter file. The table should be populated as below:

![<File:flash2.png>](flash2.png "File:flash2.png")

 Finally, change the **Download Only** drop down menu to**Firmware
Upgrade** and click on the **Download** button. Connect your Gemini and
restart it. . Once rebooted, the flash tool will detect the phone and it
will update the OS with the selected firmware.

## Linux dual boot notes

The dual boot mechanism works as follow:

-   If you restart your Gemini normally (i.e. no special key is
    pressed), then Android will start.
-   To start in recovery mode, keep pressed the Esc (On) key until the
    screen turns ON.
-   To boot Linux, keep pressed the side button key until the screen
    turns ON.