This page provides information about running Sailfish 2 Community
Edition on your Gemini. Note that this version has been replaced by the
release of [Sailfish 3 Beta for Gemini Community
Edition](Sailfish_OS_Notes "wikilink").

## <span id="Linux_boot_notes" class="mw-headline">Setting up Sailfish OS</span>

<span class="mw-headline">When setting up Sailfish OS for the very first
time, the first few screens will be in portrait mode, as in the
screenshot below:</span>

<span class="mw-headline">![](Screen_Shot_2018-06-21_at_16.22.12.png "Screen_Shot_2018-06-21_at_16.22.12.png")</span>

<span class="mw-headline">After the first few portrait screens, you will
be able to experience Sailfish OS in landscape mode:</span>

<span class="mw-headline">![](sail.jpg "sail.jpg")
In case your system start directly with the PIN screen as in the picture
above, please restart your machine as otherwise the setup configuration
is known to not complete properly. If the problem persists, try
re-flashing the linux and the sailfish_boot partition (either boot2 or
boot3) only. It has been reported that reflashing the linux and
sailfish_boot partition fixes the issue,
we</span><span class="mw-headline"> are investigating this. Also you can
read other user discussing this topic here:
[<https://together.jolla.com/question/190475/problem-installing-sailfishos-community-edition-on-gemini/>](https://together.jolla.com/question/190475/problem-installing-sailfishos-community-edition-on-gemini/).

</span><span id="Linux_boot_notes" class="mw-headline"></span><span id="Linux_boot_notes" class="mw-headline"></span>

## <span class="mw-headline">Power key and Esc (On) key</span>

On Sailfish, the Esc (On) key sends the an escape character. To send a
power event, use the key combination: Fn + Esc (On).

When you boot Sailfish OS for the first time, a few things are
initialised and the screen might turn black because of the screen
timeout. If that happens, just press Fn + Esc (On) to send a power event
and wake up the screen, or simply close your Gemini and open it again.

To power off the unit, press and hold Fn + Esc (On) for a few seconds
until the poweroff menu appear on screen.

## <span id="Known_Bugs" class="mw-headline">Known Bugs</span>

-   <span class="mw-headline">Sailfish OS is not yet available in the
    default Boot 1 position. This is due to a bug we found when the
    device is in charging mode. We are working on this!</span>
-   <s><span class="mw-headline">The optional rear-facing camera
    currently displays the image rotated by 180 degrees in Sailfish OS,
    we are investigating the issue.
    </span></s>The wrong orientation of the optional camera in Sailfish
    OS is now fixed. You can download the updated image using the
    \[partitionTool.html partition tool\], while  the updated files are
    available
    [here](https://support.planetcom.co.uk/download/camera_rotation.zip)

## <span id="Linux_boot_notes" class="mw-headline">Linux boot notes</span>

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

## <span class="mw-headline"> </span><span id="Linux_boot_notes" class="mw-headline"></span><span id="Linux_boot_notes" class="mw-headline">Updating Android on a Android/Linux Gemini </span>

Check out our updated [Android Manual Update
page](Android_Manual_Update "wikilink").