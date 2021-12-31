# rpi-infobildschirm

## installation of the operating system

1. flash a micro SD card with the newest version of Raspberry Pi OS (necessary software can be downloaded [here](https://www.raspberrypi.com/software/)
2. copy a empty file named `ssh` to the flashed micro SD card
3. when you want to connect the Pi to a wireless network, copy also the `wpa_supplicant.conf` file over to the card and adjust the `ssid` and `psk` parameters in this file
4. After the first boot, update the system with following commands:
```sh
sudo apt-get update && sudo apt-get upgrade -y 
sudo rpi-update -y
sudo apt-get autoremove -y
sudo apt-get autoclean -y
sudo reboot
```
5. After that, the Pi will restart


## dependencies in Raspberry Pi OS

Please ensure following software is installed on the pi's to ensure that everything will run properly.

- chromium browser (should be preinstalled)

- unclutter (for hiding the mouse cursor)
```sh
sudo apt-get install unclutter
```


## software setup

1. Open up the autostart config file with `sudo nano /etc/xdg/lxsession/LXDE-pi/autostart`
2. Replace the content of this file with the `autostart` file from this repo
3. Save the file and close the text editor
4. Reboot the pi with `sudo reboot`

