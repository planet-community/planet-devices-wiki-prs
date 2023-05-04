If you have a standard Android installation on your Gemini, then you
will benefit from over-the-air Android updates.

However, if you used the [Gemini Partition
Tool](http://support.planetcom.co.uk/partitionTool.html) to create a
custom Gemini partition table, for example to obtain a custom multi-boot
Linux/Android installation or a rooted Android, then you will have to
update Android manually.

This section will guide you through the process of manually update
Android on a Gemini.

**Note: Before starting is always a good idea to backup any important
data, in case things go wrong!**

For this process you will need 2 things:

-   the updated Android Base firmware
-   the unique custom scatter file created for your Gemini by the Gemini
    Partition Tool.

Let's start by downloading the updated Android Base firmware. To do
that, simply visit the [Gemini Partition
Tool](http://support.planetcom.co.uk/partitionTool.html) page, select
your Gemini version (Gemini x27, x25 or WIFI only) and click on the
**Download Base Firmware** button. Make sure you select the right
firmware for your
Gemini. <span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">If
you are not sure about your Gemini version, just check under Settings
-\> Wireless & networks. If you see a menu called SIM cards, then you
have an x27 Gemini, otherwise you have an x25 Gemini.</span>

Once you downloaded the Base firmware, unzip it to reveal the firmware
folder, for example Gemini_x27_08102018. Next, simply copy your custom
scatter file into that folder. Finally, use the Flashing Tool to write
the updated Android firmware on your Gemini. You can refer to the
[Android Flashing
Guide](http://support.planetcom.co.uk/index.php/Android_Flashing_Guide)
to download and install the Flashing Tool for Windows and for Linux.

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">Once
installed, you will need to configure it using the custom scatter file
inside the Android base firmware. See the following screenshot for
reference:</span>

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">![](Screenshot_2018-10-17_at_18.26.35.png "Screenshot_2018-10-17_at_18.26.35.png")</span>

The most important thing here is to untick the userdata partition, which
contains your data, so that your information is not deleted from the
device. If you accidentally flash the userdata partition as well, then
all your data will be lost. If you have a custom multi-boot Gemini as
used in the screenshot, then most likely a few other partitions will
already be deselected (in the screenshot, you can see that the boot,
linux and boot2 partition are deselected), this is fine. As a rule of
thumb, at least the system partition and one of the boot partition
(boot, boot2 or boot3) should be selected. Make sure you selected the
**Download Only**option.

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>To start
the flashing process, just click the big **Download** button, connect
your Gemini to your PC and restart the Gemini. Once booting, the flash
tool will detect the unit and will start flashing the device with the
selected firmware.

</div>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial="" text-decoration-color:=""\>The
following screenshot shows a successfully completed flashing process:

</div>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial=""
text-decoration-color:=""\>![](Screen_Shot_2018-06-21_at_12.08.02.png "Screen_Shot_2018-06-21_at_12.08.02.png")

</div>