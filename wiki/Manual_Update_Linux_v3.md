You can update an existing Cosmo Linux distribution to the latest 
release v3.

To make use of all the new features, you first need to manually update
your CoDi firmware to version v15, [by following this
guide](https://support.planetcom.co.uk/index.php/Linux_for_Cosmo#Requirement_2_-_Codi_firmware_v15).

Before updating, you will have to import the gemian repository key in
your device by using this command:

`curl `[`https://gemian.thinkglobally.org/archive-key.asc`](https://gemian.thinkglobally.org/archive-key.asc)` | sudo apt-key add -`

You can now update your Linux distribution using the following commands:

`sudo apt update`

`sudo apt install dialer-app address-book-service codi-app`

You can now reboot the unit to complete the installation.

To see some of the new features, please take a look at this Cosmo
Communicator update video
[<https://youtu.be/aljMVuzT5-Y>](https://youtu.be/aljMVuzT5-Y)