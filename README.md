MicroPythonESP8266
=====

MicroPython built for the ESP8266 WiFi module

https://github.com/micropython/micropython

https://github.com/themadinventor/esptool.git


Installation
--------------

Get the ESP8266 into flashing mode and then execute the following command to write the combined firmware image to the device.

This is an example on OSX using an FTDI USB capable to connect to a ESP8266-01 device     
     

    esptool.py --port /dev/cu.usbserial-A50285BI write_flash 0 firmware-combined.bin

    
    
Take the device out of flashing mode and reset.

Use the following command from the terminal to access the Python prompt


    screen /dev/cu.usbserial-A50285BI 115200
    
    
    Micro Python v1.4.4-160-g1934dca on 2015-08-03; ESP module with ESP8266
    Type "help()" for more information.
    >>> print('Hello World')
    Hello World
    >>>
    
    
Examples
----------

    import network
    network.scan(print)
    
    network.connect('{your ssid}','{your password}')
    
    #Custom ashtons firmware that has an added method for setting working mode
    network.setopmode(network.STATION_MODE)
    
    
