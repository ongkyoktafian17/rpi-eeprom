# rpi-eeprom
This repository contains the scripts and pre-compiled binaries used to create the rpi-eeprom package which is used to update the Raspberry Pi4 bootloader EEPROM.

# Support
For bootloader support the best place to start is the Raspberry Pi [General Users forum](https://www.raspberrypi.org/forums/viewforum.php?f=63) or for discussion of beta releases try the [Advanced Users forum](https://www.raspberrypi.org/forums/viewforum.php?f=29&sid=9bbc277968ad953e77749b255d0ce3a2)

N.B. Direct e-mail support questions will be ignored.

# Rescue image
If the Raspberry Pi4 is not booting, then it's very unlikely that the EEPROM is corrupted. The first thing that you should check is that the OS image was correctly installed using the Raspberry Pi Imager which is available on the [downloads page](https://www.raspberrypi.org/downloads/). If that doesn't work or you wish to revert EEPROM configuration changes to factory defaults then you can also create an EEPROM recovery SD card image using the Raspberry Pi Imager.

# Bootloader documentation
* [The boot folder](https://www.raspberrypi.org/documentation/configuration/boot_folder.md)
* [Config.txt boot options](https://www.raspberrypi.org/documentation/configuration/config-txt/boot.md)
* [Bootloader EEPROM](https://www.raspberrypi.org/documentation/hardware/raspberrypi/booteeprom.md)
* [Bootloader configuration](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bcm2711_bootloader_config.md)

# Bug reports
Bootloader bugs are especially difficult to describe because there's no display. Where possible please include the following information in order to help identify the problem.
* EEPROM version (vcgencmd bootloader_version or the pieeprom filename)
* EEPROM config (from rpi-eeprom-config)
* UART trace using USB serial cable
* Wireshark trace for network boot. Filtering for DHCP and TFTP protocols or by mac-address for the Pi4 is fine.

# BETA versions of the bootloader
If you want to try the BETA version of the bootloader then we recommend that you always try this with a spare sd-card and are familiar with using the Raspberry Pi Imager to create recovery images to restore factory settings. For debugging you may find a USB serial cable useful.

See also - [Firmware release status](https://www.raspberrypi.org/documentation/hardware/raspberrypi/booteeprom.md)

Beta features are always documented [here](https://github.com/raspberrypi/rpi-eeprom/blob/master/firmware/release-notes.md) first. Once the configuration has stabalised then the [Bootloader configuration](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bcm2711_bootloader_config.md) will be updated, however, there's normally a bit of a delay in order to allow official documentation to be reviewed.

