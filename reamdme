Flashing firmware on MCU

Flashing the new firmware to the FYSTEC SPIDER is best to be done via Micro USB. Log in on via SSH.
3d-dark.local
To compile new firmware to
cd ~/klipper/
make menuconfig

check the following options in menuconfig:
 
 
 
 
 
 

Save the configuration and exit.
Compile the firmware:
make
copy the firmware to the SD-card and rename it to firmware.bin
reinstall the sd-card and flash it.

If there is still a config mismatch due to an old klipper firmware running on the raspberry it needs updating to.
cd ~/klipper/
sudo cp "./scripts/klipper-mcu-start.sh" /etc/init.d/klipper_mcu
sudo update-rc.d klipper_mcu defaults

From ( https://www.klipper3d.org/RPi_microcontroller.html )
Building the micro-controller code¶
To compile the Klipper micro-controller code, start by configuring it for the "Linux process":
cd ~/klipper/
make menuconfig
In the menu, set "Microcontroller Architecture" to "Linux process," then save and exit.
To build and install the new micro-controller code, run:
sudo service klipper stop
make flash
sudo service klipper start
If klippy.log reports a "Permission denied" error when attempting to connect to /tmp/klipper_host_mcu then you need to add your user to the tty group. The following command will add the "pi" user to the tty group:
sudo usermod -a -G tty pi


In the menuconfig for klipper running on linux:
 



