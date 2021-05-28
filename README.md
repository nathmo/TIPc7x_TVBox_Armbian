# TIPc7x_TVBox_Armbian
a repository containing the file and the intruction to run Armbian from a TIPc7x TV box sold by AVIQ (might work on A95X from NEXBOX. not tested)

==Requirements==

* USB cable type Male A to male A (you can either make one using two USB cable that you cut and solder together, or you can order one from [https://www.aliexpress.com/item/4000097120453.html Aliexpress]
* A Computer running windows with Admin rights
* a microSD card with a reader to access it from the computer
* HDMI cable
* HDMI screen
* USB keyboard (preferably with a U.S. layout)
* a TIPc7x
* a suitable power supply for the TIPc7x
* the file in this repo

==Steps==

1) Download the required Files and extract them

2) Install the USB Burning Tool from Amlogic provided in the bundle

3) Launch the USB Burning Tool
[[File:AmLogicBurnTool.jpg|none|thumb|1280x1280px|Amlogic Burn Tool]]

4) Plug the USB cable into the USB port that is closest to the Ethernet port on the board and plug the other end in the computer.
[[File:TIPc7xAndPCAmLogicUSBBurnTool.jpg|none|thumb|1280x1280px]]
Use the correct USB port (the closest to the Ethernet port)

5) Select the ROM image to burn it
[[File:AmlogicROMSelectionMenu.jpg|none|thumb|1280x1280px]]
[[File:AmlogicROMSelectionMenuList.jpg|none|thumb|1280x1280px|Use the ROM [S905X]]]

6) Burn the Stock android ISO and stop the process between 25% and 80% (the idea being of corrupting the android ROM but not the bootloader so that it fall back to the SD card)
[[File:StoppedBurningToCorrupteFirmware.jpg|none|thumb|1280x1280px]]

7) unplug the TV box from the USB cable

8) use Rufus to burn Armbian to an SD card
[[File:RufusBurnArmbianTIPc7x.jpg|none|thumb|1142x1142px]]

9) Plug the SD card into the TIPc7x

10) Plug the HDMI into the TIPc7x and plug the other end to the screen

11) Plug the USB keyboard into the TIPc7x

12) plug the power cable into the TIPc7x

13) Wait patiently. The LED of the TIPc7x should blink between blue and red after a few seconds

14) You should see armbian booting on screen. You can now use the keyboard to set a root password and a user account. (beware, the keyboard as the American layout. Check before setting password)
[[File:ArmbianBootingTIPc7x.jpg|none|thumb|1280x1280px]]

15) launch the script to burn the OS to the eMMC memory so that you don't need an SD card to boot.
