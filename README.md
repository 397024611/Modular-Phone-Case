# Modular-Phone-Case
This phone case is designed for iPhone which can help users to extend their phones‘ functionalities

In this Repo, there will severial folders which contains infomation of each part of the phone case which includes code, electronic components set up, 3D model and logic flow diagrams. I named the phonecase as BlockCase.

Block case follows I2C protocol, the case itself is called "base" which is the master or core component of the device. Any other modulars are called "module" which are the slave of "base".

Control theory
Users enter case-control APP installed in their iPhone and select functionalities they want. For each functionality, it will have a built-in MCU address, this address will then be send to master via bluetooth, when master receives the address, master will attempt to communicate with coressponding module, if coressponding module not exists, no responding, if it exists, module ACK. The master will then send command to module and exchange data, result will send back to Phone terminal and show to users.

