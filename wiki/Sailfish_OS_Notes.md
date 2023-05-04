This page provides information about running Sailfish 3 Beta Community
Edition on your Gemini. The old notes about Sailfish 2 Community edition
are available [here](Sailfish_OS_2_Notes "wikilink").

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

## Known Bugs

-   <span class="mw-headline">Esc (On) sends the power key instead of
    ESC
    </span>
-   Volume bar gets stuck on screen when adjusting with 3 fingers
-   App covers are aligned too low on portrait orientation
-   Portrait view is broken on Calendar
-   App grid hint is not showing correctly on home screen
-   Bluetooth paring dialog is not centered on landscape
-   Security code screen does not fit to landscape view
-   Camera app settings does not show resolution
-   Brightness control keys do not work
-   Bluetooth address is not visible on settings page
-   Calculator does not work with Gemini keyboard
-   Security code/PIN code can not be typed with HW keyboard

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