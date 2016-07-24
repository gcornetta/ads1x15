# ads1x15
TI ads1x15 AD converter I2C drivers for raspberry pi-3 running node.js.
This software is provided with no guarantees.

Supported devices:
1- TI ADS1015 (12-bit AD Converter)
2- TI ADS1115 (16-bit AD Converter)

Software Configuration:
node.js version: 4.4.7
npm version    : 3.10.5

Required packages:
1- sleep
2- i2c-bus

you can download and install these packages from npmjs.org using npm.

Hardware compatibilty:
This software have been tested with a raspberry pi-3 model revision number: a02082.
You can find the hardware information typing "cat /proc/cpuinfo" on your raspberry pi-3.
The software should run without any problem on all the raspberry pi models with I2C bus address = 0x48.
Install the i2c tool (sudo apt-get install i2c-tools) to retrieve information on your I2C interface.
Don't forget to enable the I2C bus first by using "sudo raspi-config".

File description:
1- ADS1x15.js                        : class with the driver methods. Please refer to the code for further explanations
2- I2C.js                            : i2c-bus wrapper class. Encapsulates the methods provided by the i2c-bus package
3- /tests/ads1x15_ex_differential.js : sample test program

Compatibility issues:
This software is not compatible with node.js v. 6.x because the constructor of the Buffer object used in I2C.js is
deprecated in node.js v. 6.x. To solve this issue you have to change the Buffer instances on lines 63 and 78 of I2C.js
with the new instantion method defined in node.js v. 6.x. Please, refer to node documentation to learn how to do that.

