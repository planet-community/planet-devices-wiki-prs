## Android 8.1 manual upgrade for Gemini 4G (x25 and x27)

**NOTE: Some users reported problems with Android 8.1 and it's currently
recommended to use Android 7 for Gemini devices.**

**Android 8 can still be manually installed by using SP Flash Tool
following this guide: [Gemini Firmware](Gemini_Firmware "wikilink").
**

** **

<span style="color: #ff0000;">**The rest of this guide is now deprecated
and left as reference only.**</span>

**Please note this guide is for Gemini 4G devices only (both x25 and x27
models), not for Gemini WIFI devices.**

The following guide will help you to install the Android 8.1 upgrade on
your Gemini 4G, both x25 and x27 model. This guide is for an
Android-only Gemini firmware. For multi-boot firmware, please see the
[Linux Flashing Guide](Linux_Flashing_Guide "wikilink") together with
the updated [partition
tool](https://support.planetcom.co.uk/partitionTool.html).

If you have trouble updating your Gemini using the over-the-air udpate
mechanism you can follow the guide below to perform a manual upgrade.

**IMPORTANT INFORMATION for users in Japan on the NTT DoCoMo network:
<span style="color: #ff0000;">we had some reports that the network is
not detected by the Android 8 firmware. We are investigating - please
wait to upgrade your Gemini until further information is provided
</span>**

To proceed, start by running the Firmware Update application. Inside
Settings, scroll to the bottom and tap on 'About phone'.

![](Screenshot_20190507-084800.png "Screenshot_20190507-084800.png")

 

Next, tap on the first option 'Firmware Update'.

![](Screenshot_20190507-084804.png "Screenshot_20190507-084804.png")

A new version should be detected, please make sure you are connected to
a WIFI network.

![](Screenshot_20190508-134811.png "Screenshot_20190508-134811.png")

![](Screenshot_20190508-134815.png "Screenshot_20190508-134815.png")

By tapping on the Download button you will start the firmware update
download. If the download completes successfully you will just need to
tap on the 'Install Now' button to start the update process and then tap
'Firmware Update' to complete it. In case you have troubles downloading
the update, please continue with the guide.

If your download stops and cannot complete successfully you can complete
the process manually. To do that, first tap on the square button on the
soft keys (bottom right) as in the picture below to bring up the task
manager.

![](Screenshot_20190508-134832.png "Screenshot_20190508-134832.png")

After that, close the Firmware Update by swiping it out of the list as
in the following screenshot.

Now, run the File Manager application and look at the root folder in
Internal Storage. You should see a file called ota.zip. Delete the file
by selecting it with a long tap and tap and then using the Delete 
action on the menu that appears when tapping on the 3 dots button as in
the following screenshots.

![](Screenshot_20190508-134903.png "Screenshot_20190508-134903.png")

![](Screenshot_20190508-134906.png "Screenshot_20190508-134906.png")

After that, you can download the firmware from a different location:
[<http://support.planetcom.co.uk/download/Android8_4G/ota.zip>](http://support.planetcom.co.uk/download/Android8_4G/ota.zip).
It's easier to download this archive directly from your Gemini, where
you just need to open a browser and point it to the URL above. The file
will be downloaded in your Download folder.

You can also download the file on a computer and copy it to your Gemini
Download folder at a second stage.

Once the file is downloaded, open the File Manager application

![](Screenshot_20190507-084642.png "Screenshot_20190507-084642.png")

In File Manager, browse the Download folder inside the Internal Storage
to reveal the downloaded ota.zip archive. Make sure that the file you
just downloaded was not been saved with a different file name. In that
case rename the file to ota.zip.

![](Screenshot_20190507-084700.png "Screenshot_20190507-084700.png")

Next, we will have to copy the ota.zip file inside the root folder of
the Internal Storage. To do that, simply long tap the ota.zip file to
select the file and then use the copy icon that will appear once the
file is selected, as in the following screenshot.

 ![](Screenshot_20190507-084706.png "Screenshot_20190507-084706.png")

After that simply go back to the content of the root folder of Internal
Storager.

 Now, tap on the paste icon to paste the ota.zip file in the root
folder.

![](Screenshot_20190507-084723.png "Screenshot_20190507-084723.png")

 

Please note that if you already have a file called ota.zip, then the
just copied file will be renamed with an extension. In that case, please
remove the ota.zip file in the root folder of your Internal Storage and
copy/paste the file again.

Now that we copied the update archive in the correct location, we need
to start the update process. Inside Settings, scroll to the bottom and
tap on 'About phone'.

![](Screenshot_20190507-084800.png "Screenshot_20190507-084800.png")

 

Next, tap on the first option 'Firmware Update'.

![](Screenshot_20190507-084804.png "Screenshot_20190507-084804.png")

Now, inside the Firmware Update application, tap on the settings icon,
in the top right of the screen.

![](29.jpg "29.jpg")

Inside settings, tap on Manual Update.

![](32.jpg "32.jpg")

 

You should then be presented with a screen as in the screenshot below.
Tap on 'Install Now' option on the left.

![](01.jpg "01.jpg")

A confirmation dialog will then appear. By tapping  on the 'Firmware
Update' button you will start the update procedure. Note the the button
might be not fully visible in landscape mode.

![](22.jpg "22.jpg")

Your Gemini will then reboot and complete the update. Once the update is
completed you will see the following message.

![](Screenshot_20190507-085946.png "Screenshot_20190507-085946.png")

Please note that the Android 8.1 update might trigger a number of
upgrade scripts and application updates. As a result your device might
appear slower and feel hotter than usual for some time.

## Notes on using your Gemini with Android 8.1 

### Re-starting and booting Android 8.1 for the first time

<div style='color: #000000; text-align: start; text-decoration: none;'>

The first boot of the ungraded Android 8 Gemini will take a while as the
system is booting for the first time.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

Once the Gemini has restarted, it will still take some time until the
installation is fully complete. You will get an on-screen message that
the Android update is complete. After that the device may still feel a
bit sluggish as file formats and data is being adapted for each
application to Android 8 formats. This process should last a maximum of
few hours, but it is dependent on the storage of your device. The more
data you have the longer the process may take. You may feel the device
even getting warm from the processing of this data. 

</div>

### Android 8 security 

<div style='color: #000000; text-align: start; text-decoration: none;'>

Because the security frameworks are different in Android 8 and Android
7, you may be asked to re-authenticate your Google or other accounts as
well as to re-grant permissions for the apps that you are running.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

Typically you will be asked to grant specific permissions with an
on-screen message.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

If you notice any apps crashing, this may be because they are simply not
compatible with Android 8. Please check in Settings-\>Apps if all the
required permissions have been granted to the app that is crashing, just
in case it is a security issue.

</div>

### New features in Android 8

<div style='color: #000000; text-align: start; text-decoration: none;'>

**<img src="Screenshot_20190508-135353.png"
title="Screenshot_20190508-135353.png" width="800" height="400"
alt="Screenshot_20190508-135353.png" />**

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

We have introduced some new settings for the Gemini in Android 8.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

You can now move the Android Navigation bar from the right hand side of
the screen to the left hand side using the "Move Navigation Bar to the
left side" setting.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

You can also completely remove the Android Navigation bar from the
screen by using the "Hide Navigation Bar" setting.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

You will need to restart the Gemini for this feature to take effect. 

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

When the Navigation Bar is hidden you will need to use the keyboard
shortcuts for the Go Back, Go to Desktop and Apps list functions.

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

The keyboard shortcuts for Go Back, Go to Desktop and Apps list are as
follows:

</div>

-   Back - Esc (escape key)
-   Desktop - Fn + d
-   Apps - Fn + a

<div style='color: #000000; text-align: start; text-decoration: none;'>

There is a new keyboard shortcut to rotate the screen:

</div>

-   Shift + Fn + R will rotate the screen from landscape to portrait and
    vice versa.

<div style='color: #000000; text-align: start; text-decoration: none;'>

<figure>
<img src="Screenshot_20190508-135359.png"
title="Screenshot_20190508-135359.png" width="800" height="400"
alt="Screenshot_20190508-135359.png" />
<figcaption
aria-hidden="true">Screenshot_20190508-135359.png</figcaption>
</figure>

</div>
<div style='color: #000000; text-align: start; text-decoration: none;'>

The new App Bar is now scrollable. You can scroll left and right and
extend the number of app icons in the app bar.

</div>

### Reporting issues

<div style='color: #000000; text-align: start; text-decoration: none;'>

Please report any issue with Android 8 on Gemini to
support@planetcom.co.uk

</div>

## Known Bugs

-   LEDison has been reported to crash under some circumstancies - we
    will update the application in the Play Store soon
-   It has been reported that sometimes the Micro SD may 'disappear' -
    we are investigating, but if this happens to you, just reboot your
    Gemini
-   The Factory Reset does not work on Android 8 - we are investigating
    this