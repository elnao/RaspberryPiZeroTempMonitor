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
- `sudo apt-get update`
- `sudo apt-get upgrade`
- `sudo apt-get install python3-pip` 
- `sudo pip3 install --upgrade setuptools`
- `sudo pip3 install --upgrade adafruit-python-shell`
*Above instructions can be found at: https://web.archive.org/web/20210207181436/https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/installing-circuitpython-on-raspberry-pi*

