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
*Above 5 commands can be found at: https://web.archive.org/web/20210207181436/https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/installing-circuitpython-on-raspberry-pi*
- `sudo pip3 install adafruit-circuitpython-busdevice`
- `sudo pip3 install adafruit-circuitpython-bme280`
*Above command can be found at: https://web.archive.org/web/20210207224604/https://github.com/adafruit/Adafruit_CircuitPython_BME280*
- `sudo apt-get install python3-rpi.gpio
*Above command was found at: https://web.archive.org/web/20210208024441/https://raspberrypi.stackexchange.com/questions/60774/importerror-no-module-named-rpi*


### Create Demo Script and Test Temp Sensor
- `sudo nano temp_demo.py`
- Copy the contents of the usage example at the below page into the nano editor.
*https://web.archive.org/web/20210207224604/https://github.com/adafruit/Adafruit_CircuitPython_BME280*
- Save and exit nano
- run `python3 temp_demo.py`

### Install Flask Web Server
- `sudo apt install python3-flask`
- *follow instructions at https://www.instructables.com/Python-WebServer-With-Flask-and-Raspberry-Pi/*

### Render CSV Data in HTML
- `sudo pip3 install pandas`
- *follow instructions at https://www.codespeedy.com/converting-csv-to-html-table-in-python/*

