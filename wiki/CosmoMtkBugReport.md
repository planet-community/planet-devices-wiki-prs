The following is a step-by-step guide thta can be used to send detailed
bug report to Planet Computers.

Thank you for your cooperation!

## Enable USB debugging

To be able to send detailed bug reports you will need to enable USB
debugging first.

-   Press Fn+Del to go to Settings and scroll down to the bottom of the
    list and select System
    ![](Screenshot_20200626-155348.png "Screenshot_20200626-155348.png")
-   Scroll down to the bottom of the list and select Advanced
    ![](Screenshot_20200626-154452.png "Screenshot_20200626-154452.png")
-   Scroll down to the bottom of the list and select About phone
    ![](Screenshot_20200626-154504.png "Screenshot_20200626-154504.png")
-   Scroll down to the bottom of the list and tap on Build number
    multiple times until you see the "You are now a developer" screen
    ![](Screenshot_20200626-154517.png "Screenshot_20200626-154517.png")
-   Now, go back and select Developer options
    ![](Screenshot_20200626-155124.png "Screenshot_20200626-155124.png")
-   Finally, scroll down and activate the USB debugging option

![](Screenshot_20200626-200519.png "Screenshot_20200626-200519.png")

![](Screenshot_20200626-200524.png "Screenshot_20200626-200524.png")

![](Screenshot_20200626-200535.png "Screenshot_20200626-200535.png")

## Enable MTK Logger

-   Start the dialler application and type the following code:
    \*#\*#3646633#\*#\*
    ![](Screenshot_20190528-101517.png "Screenshot_20190528-101517.png")
-   Go to the Log and Debugging tab and tap on MTKLogger
    ![](Screenshot_20200626-200638.png "Screenshot_20200626-200638.png")
-   Inside MTKLogger, tap on the option button (top-right)
    ![](Screenshot_20200626-200645.png "Screenshot_20200626-200645.png")
-   And enable the Tag Log functionality
    ![](Screenshot_20200626-200707.png "Screenshot_20200626-200707.png")
-   Finally, press the start button to start saving logs.

![](Screenshot_20190528-101549.png "Screenshot_20190528-101549.png")

##  Saving logs

After the last action, logs are now being saved on the device. It's a
good idea to restart the unit at this point, so that any log related to
device initialisation is also recorded. After reboot, please repeat the
action that causes the trouble. When the issue has been reproduced,
simply scoll down form the top to reveal the MTKLogger menu and stop the
logger.

![](Screenshot_20190528-101604.png "Screenshot_20190528-101604.png")

## Sending the logs to Planet Computers

The logs created by MTKLogger are in the /mtklog folder in the Internal
Storage (Cosmo_Communicator).

One way to send the logs back to Planet Computers is to compress the
/mtkfolder and send it to **cosmobugreport@planetcom.co.uk** using a
cloud service, such as
[<https://www.mailbigfile.com>](https://www.mailbigfile.com)

1.  Open Files by Google
2.  Tap on the additional option icon (the three vertical dots icon
    located top-right) and select 'Show internal storage'
3.  Navigate to the Cosmo_Communicator and long-tap on the mtklog folder
4.  Tap again on the additional option icon and select 'Compress'. This
    will create the file 'mtklog.zip' in the root of
    'Cosmo_Communicator'

You can now send the file using  a cloud service.

Alternatively, you can connect your Gemini to a computer, copy the
mtkfolder to the computer, compress it and then send it to
**cosmobugreport@planetcom.co.uk** using a cloud service, such as
[<https://www.mailbigfile.com>](https://www.mailbigfile.com)

![](Screenshot_2019-05-28_at_10.28.13.png "Screenshot_2019-05-28_at_10.28.13.png")
![](Screenshot_2019-05-28_at_10.28.47.png "Screenshot_2019-05-28_at_10.28.47.png")