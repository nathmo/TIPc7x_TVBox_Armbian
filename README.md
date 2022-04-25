# TIPc7x_TVBox_Armbian (VTX TV)
a repository containing the file and the intruction to run Armbian from a TIPc7x TV box sold by AVIQ (maybe known as VTX TV box)

## Disclaimer

This procedure is not 100% safe and there is a risk of leaving your board in a unsusable state.You have been warned.
If you encounter spelling mistake, imprecision in the steps, or any other problem with thoses instruction or file dont hesistate to open an issue or directly a pull request and if you find this tutorial useful please star this repo.

## Requirements

* USB cable type Male A to male A (you can either make one using two USB cable that you cut and solder together, or you can order one from [https://www.aliexpress.com/item/4000097120453.html]
* A Computer running windows with Admin rights
* a microSD card with a reader to access it from the computer
* HDMI cable
* HDMI screen
* USB keyboard (preferably with a U.S. layout)
* a TIPc7x
* a suitable power supply for the TIPc7x
* the file in this repo


## Acknolegments
Thanks to Luigi Petrucci for the hints that saved me hours of pain.
Thanks to the stranger online who provided bit and part of information to compile linux for the beast.

## Steps

1) Download the required Files and extract them

2) Install the USB Burning Tool from Amlogic provided in the bundle

3) Launch the USB Burning Tool

![Amlogic UI](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/AmlogicBoot.jpg)

4) Introduce a rod (contton swap that you cut work great) in the jack port until you fell a little click. then, Plug the USB cable into the USB port that is closest to the Ethernet port on the board and plug the other end in the computer. Dont forget to keep the button in the jack port pressedn when you plug the USB cable in. THis force the device to boot in debug mode

![USB cable setup](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/USBCableSetup.jpg)

Use the correct USB port (the closest to the Ethernet port)

5) Select the ROM image to burn it

![Click there](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/AmlogicImportImage.jpg)

![ROM selction menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/AmlogicROMSelection.jpg)

![Beginning of the burn process](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/AmlogicBurnStockAndroidBeginning.jpg)

6) Burn the Stock android ISO and stop the process between 25% and 80% (the idea being of corrupting the android ROM but not the bootloader so that it fall back to the SD card)

![Stop after 25%](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/AMLogicBurnStopCorruptFallback.jpg)

7) unplug the TV box from the USB cable

8) use Rufus to burn Armbian to an SD card

![Rufus UI with the profer image selected and the sd card ready](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/RufusReady.jpg)

9) Plug the SD card into the TIPc7x

10) Plug the HDMI into the TIPc7x and plug the other end to the screen

11) Plug the USB keyboard into the TIPc7x

12) plug the power cable into the TIPc7x

13) Wait patiently. The LED of the TIPc7x should blink between blue and red after a few seconds

14) You should see armbian booting on screen. You can now use the keyboard to set a root password and a user account. (beware, the keyboard has the American layout. Check before setting password)

![Armbian Boot](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianBootingHDMIScreen.jpg)

15) once the box reboot you can login with the account you created and launch "sudo armbian-config"

![Armbian Login](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianInstalleMMC.png)

16) Now select system 

![Armbian config main menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianeMMC2.png)

17) Now select Install 

![Armbian config menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbaineMMC3.png)

18) Now select Boot from eMMC

![Armbian config menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianeMMC5.png)

19) say yes

![Armbian config menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianeMMC7.png)

20) choose ext4 formating

![Armbian config menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbaineMMC8.png)

21) wait

![Armbian config menu](https://github.com/nathmo/TIPc7x_TVBox_Armbian/blob/main/Pictures/ArmbianeMMC9.png)

22) Once it's done you can remove the sd card and run "sudo reboot now" and the board should now boot on Armbian from the eMMC memory
