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
- `sudo pip3 install adafruit-circuitpython-bme280`
*Above command can be found at: https://web.archive.org/web/20210207224604/https://github.com/adafruit/Adafruit_CircuitPython_BME280*
### Create Demo Script and Test Temp Sensor
- `sudo nano temp_demo.py`
- Copy the below script in the nano editor
`import board
import digitalio
import busio
import time
import adafruit_bme280

# Create library object using our Bus I2C port
i2c = busio.I2C(board.SCL, board.SDA)
bme280 = adafruit_bme280.Adafruit_BME280_I2C(i2c)
#or with other sensor address
#bme280 = adafruit_bme280.Adafruit_BME280_I2C(i2c, address=0x76)

# OR create library object using our Bus SPI port
#spi = busio.SPI(board.SCK, board.MOSI, board.MISO)
#bme_cs = digitalio.DigitalInOut(board.D10)
#bme280 = adafruit_bme280.Adafruit_BME280_SPI(spi, bme_cs)

# change this to match the location's pressure (hPa) at sea level
bme280.sea_level_pressure = 1013.25

while True:
    print("\nTemperature: %0.1f C" % bme280.temperature)
    print("Humidity: %0.1f %%" % bme280.relative_humidity)
    print("Pressure: %0.1f hPa" % bme280.pressure)
    print("Altitude = %0.2f meters" % bme280.altitude)
    time.sleep(2)`
