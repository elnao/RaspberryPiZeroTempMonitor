### Download and install Rasbperry PI Imager.
### Install Rasbperry PI Lite to SD card.
### Boot up your Raspberry PI Zero.
### Run `sudo raspi-config` and
- Enable SSH
- Enable i2c
- Change Password
- Add to wireless network
- Save and reboot
### Install Updates, PIP, and Python
- sudo apt-get update
- sudo apt-get upgrade
  and
- sudo pip3 install --upgrade setuptools
  If above doesn't work try
-  sudo apt-get install python3-pip
*Above instructions can be found at: https://web.archive.org/web/20210207181436/https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/installing-circuitpython-on-raspberry-pi*

