## <span id="This_Flashing_guide_is_now_marked_as_obsolete." class="mw-headline"><span style="color: #ff0000;">This page is now marked as obsolete.</span></span>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial=""
text-decoration-color:=""\><span style="color: #ff0000;">Please use the
following pages to browse the updated [Gemini Firmware
page](Gemini_Firmware "wikilink").
</span>

</div>

## Available Official Firmware

Here is the list of the latest available firmwares for your Gemini.

We have 3 firmware versions, please be sure you download the right
firmware for your device. WiFi-Only Gemini users should download the
WiFi-Only firmware. 4G Gemini users using x25 chip (early release
Geminis) should download the 4G Gemini x25 firmware. Finally, the Gemini
4G x27 users should download the 4G Gemini x27 firmware. If you are not
sure about your Gemini version, just check under Settings -\> Wireless &
networks. If you see a menu called SIM cards, then you have an x27
Gemini, otherwise you have an x25 Gemini.

#### WiFi-Only Gemini

Coming soon.

#### 4G Gemini x25 (early release)

-   [Gemini 4G x25 firmware (Android + Rooted Android + Debian Technical
    Preview
    1)](http://support.planetcom.co.uk/download/Old/Gemini_x25_11052018.zip) -
    11/05/2018
-   Please note that you will need to update your Debian Linux to enjoy
    the latest development. See
    [<https://github.com/gemian/gemini-keyboard-apps/wiki/DebianTP>](https://github.com/gemian/gemini-keyboard-apps/wiki/DebianTP)
    for further information regarding updating and configuring your
    Debian system

#### 4G Gemini x27

-   [Gemini 4G x27 firmware (Android + Rooted Android + Debian Technical
    Preview
    1)](http://support.planetcom.co.uk/download/Old/Gemini_x27_10052018.zip)-
    10/05/2018
-   Please note that you will need to update your Debian Linux to enjoy
    the latest development. See
    [<https://github.com/gemian/gemini-keyboard-apps/wiki/DebianTP>](https://github.com/gemian/gemini-keyboard-apps/wiki/DebianTP)
    for further information regarding updating and configuring your
    Debian system

Once you have downloaded the right firmware for you, please extract the
zip file and follow our [Flashing Guide
OLD](Flashing_Guide_OLD "wikilink") to install it.

Each firmware archive above contains 3 different version of the firmware
that can be installed:

-   **Standard Android firmware**
    Please use the "Gemini_Android.txt" scatter file to flash the
    Android firmware.
-   **Rooted Android firmware**
    <span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">With
    Gemini you have the option to easily root your device. Please bear
    in mind that rooting an Android device comes with associated risks,
    and some application might not work correctly. You can search the
    Internet for more information, we suggest that you proceed only if
    you know what you are doing. 
    If you know what you are  doing and you want to continue, then you
    can use the </span>"Gemini_Android_Rooted.txt" scatter file to flash
    the rooted Android firmware. Please complete the process by
    installing [Magisk Manager](https://magiskmanager.com/).
-   **Dual Boot Android/Linux
    **To install a dual boot Android/Linux image you must first
    partition your Gemini, deciding how much space to reserve for each
    system and what system you would like to boot into by default. For
    example, if you specify to boot into Android by default, then the
    Gemini will boot into Android when started. To boot into Linux, you
    will have to press the side button when booting. You can configure
    the space and the default booting system using this partition tool:
    [<http://support.planetcom.co.uk/download/Old/partitionTool.html>](http://support.planetcom.co.uk/download/Old/partitionTool.html)
    Make sure you reserve enough space for Linux, you will need around 5
    GB of space for Debian. The flash tool will show you an error
    message if the partition size is too small.
    When you have selected your parameters, click on the  "Download
    Scatter file" button to retrieve a copy of the Gemini_Dual_Boot.txt
    scatter file and place it in the folder containing the firmware. You
    can now use this scatter file to flash a dual boot Android/Linux
    firmware on your Gemini. Don't forget to check out this Web page for
    further information about

<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;"> </span>

## Team Win Recovery Project (TWRP alternative recovery image)

An unofficial build of TWRP has been ported to Gemini by
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">deadman96385</span>.

You can find more information about it here: [TWRP for
Gemini](https://forum.xda-developers.com/gemini-pda/development/recovery-twrp-3-2-1-0-t3763855)

TWRP is an alternative recovery image that can be used to install
Lineage OS. Please note that you should immediately boot into recovery
partition after installing TWRP. If you boot the stock Android firmware,
it will reinstall the original reovery partition, overwriting TWRP.

## Lineage OS preview

An unofficial builld of Lineage OS for the Gemini has been developed by
<span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">deadman96385</span>.

You can find more information about it here: [Initial release of Lineage
OS for Gemini
PDA](https://forum.xda-developers.com/gemini-pda/development/rom-lineageos-14-1-geminipda-t3770821)

## <span id="Source_Code" class="mw-headline">Source Code</span>

\<div style="margin: 0.4em 0px 0.5em; color: \#252525;" source=""
sans="" pro="" sans-serif="" font-size:="" 15="" 008px="" font-style:=""
normal="" font-variant-ligatures:="" font-variant-caps:=""
font-weight:="" 400="" letter-spacing:="" orphans:="" 2=""
text-align:="" start="" text-indent:="" 0px="" text-transform:=""
none="" white-space:="" widows:="" word-spacing:=""
-webkit-text-stroke-width:="" background-color:="" ffffff=""
text-decoration-style:="" initial=""
text-decoration-color:=""\><span style="color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration-style: initial; text-decoration-color: initial; float: none; display: inline !important;">Source
code for the Linux kernel, the bootloader and the flash tool has been
published on GitHub: 
[<https://github.com/dguidipc>](https://github.com/dguidipc)</span>

</div>