
You'll need:
 - a simple [FTDI-based](https://en.wikipedia.org/wiki/FTDI) JTAG/SPI/UART tool. [Buy one](https://www.ebay.com/itm/FT2232-USB-DIP-module-for-FTDI-FT2232D-dual-UART-FIFO-JTAG-SPI-/162159976456) or, [build one](assets/ftditool.jpg) yourself. It is a very usefull tool to have.
 - an [AT45DB011D](https://www.aliexpress.com/item/New-IC-45DB011D-AT45DB011D-SSH-B-AT45DB011D-SSH-AT45DB011D-ATMEL-SOP8/2040210560.html) IC with unprogrammed security register
 - this script to flash the security register on your AT45DB011D
 - a bunch of wires
 - a soldering iron
 - a needle
 - steady hands

Use pip to install pyftdi before running the script.

Warning: there is a fair chance of bricking your console. Do it on your own risk. 

Note: The security register inside an AT45DB011D is OTP (one time programmable). 
If you mess it up, there will be no second chance with the same IC. Buy a bunch if you want to experiment a bit.

Here we go:
 - use your steady hands and a soldering iron to connect wires right to the AT45DB011D terminals
 - use [this schematics](assets/programmer.png) to connect the AT45DB011D to your FTDI JTAG/SPI tool
 - run the script
 - cut the wires so that the IC fits inside the WetherLink compartment inside the console
 - don't strip the wires
 - push a needle ~2mm deep through the end of each wire. Keep the needle straight so it won't pierce through the insulation
 - [connect the wires to the console's extension header](assets/maharaika.jpg)
 - connect UART port terminals in the same way
 - you can use your FTDI tool in serial mode to test that it works
