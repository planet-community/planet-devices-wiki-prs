# Gemini 4G x27 firmware restoration

If your Gemini firmware is being damaged or corrupted your Gemini might
be stuck in a boot loop animation screen. To restore your unit you will
need to update your Android software in your device by using the Flash
Tool. You will need a PC with either Windows or Linux to do this, we
suggest to use Windows as it has the best compatibility with the flash
tool. Please follow the steps below to update your Gemini and restore
firmware to full functionality.

### Step 1 - Install FlashTool software and drivers

 The first step is to install the flash tool drivers. These drivers are
needed for your Windows PC to communicate with your Gemini. You can find
the drivers here: [Windows Flash Tool
Drivers](http://support.planetcom.co.uk/download/FlashToolDrivers.zip)

<div style="text-align: justify;">

Once downloaded, unzip the archive and extract the files.

</div>
<div style="text-align: justify;">

You will find a folder called **FlashToolDrivers**, open the folder.

</div>
<div style="text-align: justify;">

Run the install file by double clicking on the **Install** file
(Install.bat).

</div>
<div style="text-align: justify;">

Allow the installation to complete by clicking Yes when asked to make
changes.

</div>

Now that the drivers have been installed, please download the Windows
flash tool from this link  [Windows Flash
Tool](http://support.planetcom.co.uk/download/FlashToolWindows.zip).
Please unzip the archive and extract the FlashToolWindows folder.

If you use Linux you don't need any drivers and you can proceed directly
to download the Linux flash tool on this link [Linux flash
tool](http://support.planetcom.co.uk/download/FlashToolLinux.tgz).
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">You
will need a 64 bit Linux machine and you might need root access to run
it. Unzip the archive and extract the FlashToolLinux folder.
</span>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">You
have now completed step 1.</span>

### Step 2 – Download Gemini Firmware

Download the Gemini 4G x27 firmware from this link [Gemini 4G x27
firmware](http://support.planetcom.co.uk/download/Gemini_Android_x27_v1_16032018.zip)

Unzip the downloaded archive and extract the
Gemini_Android_x27_v1_16032018 folder.

You have now completed step 2.

### Step 3 – Flashing the Android Firmware

<div style="text-align: justify;">

On Windows just run the flash tool by double clicking on the
**flash_tool** file in the **FlashToolWindows** folder.

</div>
<div style="text-align: justify;">

On Linux,
t<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">he
executable file is called **flash_tool.sh**. On Linux,
</span><span style="font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration: none; caret-color: #2b2e2f; color: #2b2e2f; font-family: 'Lucida Sans Unicode', 'Lucida Grande', Tahoma, Verdana, sans-serif; font-size: 14px; text-size-adjust: auto; float: none; display: inline !important;">If
you get a BROM error when connecting the Gemini (see flash_tool console
log) then you should follow this
guide </span>[<https://forum.xda-developers.com/general/rooting-roms/tutorial-how-to-setup-spflashtoollinux-t3160802/page16>](https://forum.xda-developers.com/general/rooting-roms/tutorial-how-to-setup-spflashtoollinux-t3160802/page16)<span style="font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration: none; caret-color: #2b2e2f; color: #2b2e2f; font-family: 'Lucida Sans Unicode', 'Lucida Grande', Tahoma, Verdana, sans-serif; font-size: 14px; text-size-adjust: auto; float: none; display: inline !important;"> -
specifically the 2 points regarding udev rules.</span>

</div>
<div style="text-align: justify;">

<span style="font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration: none; caret-color: #2b2e2f; color: #2b2e2f; font-family: 'Lucida Sans Unicode', 'Lucida Grande', Tahoma, Verdana, sans-serif; font-size: 14px; text-size-adjust: auto; float: none; display: inline !important;">The
flash tool window will now appear as in the picture below. Plea</span>se
use the **choose** buttons on the right hand side as in the following
screenshot to load set the Download-Agent (1) and the Scatter-loading
file (2):

</div>

-   Download-Agent should be set to the file **MTK_AllInOne_DA.bin**,
    which is located in the FlashToolWindows or FlashToolLinux folder.
-   Scatter-loading file should be set to the
    file**Gemini_Android.txt,** which is located in the
    Gemini_Android_x27_v1_16032018 folder.

<figure>
<img src="IMG_05062018_155929_0.png" title="IMG_05062018_155929_0.png"
width="640" height="360" alt="IMG_05062018_155929_0.png" />
<figcaption aria-hidden="true">IMG_05062018_155929_0.png</figcaption>
</figure>

<div style="text-align: justify;">

Once you have chosen the Download-Agent and Scatter-loading File, make
sure that you deselect all the items in the table except the system
partition. By flashing only the system partition, you will be able to
fix your Gemini while keeping all your data, which are stored in the
userdata partition. If you choose only your system partition, your
screen should look like the following screenshot.


</div>

<figure>
<img src="IMG_05062018_160710_0.png" title="IMG_05062018_160710_0.png"
width="641" height="360" alt="IMG_05062018_160710_0.png" />
<figcaption aria-hidden="true">IMG_05062018_160710_0.png</figcaption>
</figure>

<div style="text-align: justify;">
<div style="text-align: justify;">

Finally, select the **Download Only** drop down menu, then click on the
**Download** button as in the screenshot below.


</div>
<div style="text-align: justify;">

<figure>
<img src="Screen_Shot_2018-06-05_at_22.57.25.png"
title="Screen_Shot_2018-06-05_at_22.57.25.png" width="640" height="359"
alt="Screen_Shot_2018-06-05_at_22.57.25.png" />
<figcaption
aria-hidden="true">Screen_Shot_2018-06-05_at_22.57.25.png</figcaption>
</figure>

</div>

The flash tool will now wait for your Gemini to be connected to your PC
in firmware download mode. To achieve this now, connect your Gemini to
your PC using the USB-C cable. Then restart your Gemini by pressing the
Esc (On) key for up to 20 seconds. Once the Gemini starts rebooting, the
flash tool will detect the unit and Android will be updated. Once the
flash process is finished, disconnect the Gemini and then press and hold
the Esc (On) key until the unit restarts again.

The Gemini should now successfully boot into the updated Android
firmware.

This completes the firmware update process.

</div>