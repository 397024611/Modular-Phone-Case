# Modular-Phone-Case basic information
This phone case is designed for iPhone which can help users to extend their phones‘ functionalities

In this Repo, there will severial folders which contains infomation of each part of the phone case which includes code, electronic components set up, 3D model and logic flow diagrams. I named the phonecase as BlockCase.

BlockCase follows I2C protocol, the case itself is called "base" which is the master or core component of the device. Any other modulars are called "module" which are the slave of "base".

Control theory.

Users enter case-control APP installed in their iPhone and select functionalities they want. For each functionality, it will have a built-in MCU address, this address will then be send to base via bluetooth, when base receives the address, it will attempt to communicate with coressponding module, if coressponding module not exists, no responding, if it exists, module ACK. The base will then send commands to module and exchange data, result will send back to Phone terminal and show to users.

How base and module connect (I2C protocol, https://learn.sparkfun.com/tutorials/i2c).

For some basic modules(e.g. LED module, IR Control module), they are connected with base by four wires, which are SDA, SCL, GND, and VCC.
SCL is the clock line, enables command can be transfered or not. SDA is data line, used for data transfer. Vcc provides power to both side (master and modules). GND is ground line. Physically, base and module are connected by using tiny magnets.

