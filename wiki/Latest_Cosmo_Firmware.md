### Android Firmware update v25 - 22/03/2021

<span style="caret-color: #252525; color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008000373840332px; font-style: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: auto; word-spacing: 0px; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration: none; display: inline !important; float: none;">
This version includes keyboard firmware improvements, security patches
and bug  fixes. </span>

<span style="caret-color: #252525; color: #252525; font-family: 'Source Sans Pro', sans-serif; font-size: 15.008000373840332px; font-style: normal; font-variant-caps: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: auto; word-spacing: 0px; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; background-color: #ffffff; text-decoration: none; display: inline !important; float: none;">If
you use the rooted Android Firmware, </span>[make sure to update it by
following these instructions](Rooted_Android_For_Cosmo "wikilink").

### Android Firmware update v23 - 6/07/2020

This Android firmware release contains some improvements in the cover
display communication and bug fixes, as well as introducing the power
save setting for the Cover Display.

The Cover Display power save setting is OFF by default and can be found
in Settings -\> Cosmo Settings.

The new option is called “Cover Display Power Save”. If enabled, it will
activate a power saving functionality that will result in less power
being used when the phone is idle. With the option disabled, the
firmware will behave as the same V19 firmware.

### Android Firmware update v22 -  22/06/2020** **

The latest Android firmware update includes:

-   Modified bootloader to enable mobile radio modem and SIM cards to be
    recognised when booting into Linux, rooted Android and other
    non-Android operating systems
-   Much improved battery consumption for Cosmo in idle (sleep) mode
-   Improved screen rotation function plus soft keyboard availability
    when Cosmo screen is used in portrait mode
-   Recent Android Security and other OS Updates
-   Notes app: dictation feature can now be controlled via Cover Display
-   Data app: databasefile export and import functions
-   Improved eSIM compatibility
-   Updated Google certificate
-   Bugfixes

Please note that you will have to update your CoDi firmware as well to
take advantage of the new features. You can update the CoDi firmware by
using the Cover Display Assistant application or alternatively you can
[update the firmware manually](#Manual_CoDi_firmware_update "wikilink").

**Android Firmware update 11/12/2019**

This Cosmo firmware includes new features and solves a number firmware
issues reported by users:

1.  New settings: switch OFF cover display on power down

    ![](ndhcaeyk8nlog9t2na6s.png "ndhcaeyk8nlog9t2na6s.png")

    This feature helps saving battery when Cosmo Communicator is powered
    down by switching OFF the cover display. When powered down in this
    way, you will only be able to switch on your Cosmo using the Esc key
    and charge your Cosmo using the left hand side USB-C port. We are
    looking at further power saving firmware possibilities
2.  Fix for power charging indicator being on while the keyboard
    backlight is on.
3.  The Duraspeed and Background Power Saving settings status is now OFF
    by default. This fixes the operation of many applications which were
    reported to be closing in the background when Duraspeed is ON. Some
    services were being closed down after some time of inactivity.
4.  The eSIM chip status is now fixed after Cosmo restart, so eSIM
    selection is preserved (instead of switching to SIM lost 2)
5.  Fix for Reject ringing call during another call from cover display
6.  Fix for sending SMS reject call when two calls exist
7.  Fix for Switch calls and merge calls from cover display
8.  The Cover Display will now support the advertised landscape mode.
9.  The Cover display will also support two font sizes for notification
    text.
10. Fix for icon sensitivity on top row of icons on the cover display
11. Optimisation for Contact list update on cover display
12. Some stability fixes for cover display

## Manual CoDi firmware update

You can manually update the Codi firmware in case the automatic download
fails. The Codi firmware consists of 2 files and the latest version is
available here:

-   [Cosmo_firmware-stem_ospi2_1_1_1_14.bin](http://support.planetcom.co.uk/download/CodiLatest/Cosmo_firmware-stem_ospi2_1_1_1_14.bin)
-   [Cosmo_resource-stem_resource_1_1_1_14.bin](http://support.planetcom.co.uk/download/CodiLatest/Cosmo_resource-stem_resource_1_1_1_14.bin)

To manually update the Codi firmware, plesae download and copy these two
files on your Cosmo Communicator. After that, run the Codi Display
Assistant application, tap on the ADVANCED button and select "Flash
Image Manually". On the file selector view, you might have to tap on the
"Show Internal storage" option under the more option icon on the top
right of the screen (the icon with the 3 round dots).

Bear in mind that the file names are important - please don't rename the
files.