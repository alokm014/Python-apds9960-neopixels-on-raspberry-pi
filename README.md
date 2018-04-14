# Python-apds9960-neopixels-on-raspberry-pi
How to control NeoPixel LEDs with Gesture in Python on a Raspberry Pi!

Python library for the apds9960 with neopixels on raspberry-pi developed while I was looking to get the APDS-9960 to work with a Raspberry Pi.
First of all i would like to thank https://github.com/ThomasWaldmann for APDS-9960 library and also https://github.com/jgarff/rpi_ws281x/commits?author=Gadgetoid for neopixel library.

These two libraries is the key that makes using Gesture controlled NeoPixels Leds with the Raspberry Pi possible.
### Compile & Install Libraries ###
These steps will show you how to compile the libraries and install a Python wrapper around it.
To start, connect to a terminal on the Raspberry Pi and execute the following commands to install some dependencies:

```
sudo apt-get update  
sudo apt-get install build-essential python-dev git scons swig
```
Now run these commands to download the library source and compile it:
```
git clone https://github.com/alokm014/Python-apds9960-neopixels-on-raspberry-pi.git
cd Python-apds9960-neopixels-on-raspberry-pi
unzip python-apds9960.zip
unzip rpi_ws281x.git.zip
cd python-apds9960
sudo mv apds9960 ~/../../usr/local/lib/python2.7/dist-packages/
cd ../rpi_ws281x
scons
```
After running the scons command above you should see the library successfully compiled.  Next you can install the Python library by executing:
```
cd python
sudo python setup.py install
```
Inside the examples subdirectory you can find a couple examples of using the library.
Gesture.py is an example of using the high-level Python library which looks like the Arduino NeoPixel library. 
### Gesture.py Example
run it by executing
```
sudo python Gesture.py
```
