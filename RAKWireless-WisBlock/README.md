# RAKWireless WisBlock
![](../assets/RAK-wisblock-starter-board.png)

The WisBlock Starter Kit is just one of a line of products offered by RAKWireless. The starter kit is just that, a base developer board that can 
have multiple combinations of expansion boards added to it. The full WisBlock offering can be seen [here](https://store.rakwireless.com/pages/wisblock).

## Introduction

Here you will find one or more sample PlatformIO embedded projects designed to transmit LoRaWAN packets using a [WisBlock Starter Kit](https://store.rakwireless.com/products/wisblock-starter-kit).

## Getting Started
```
Library update notice:
Recent API changes to the runtime support library, SX126x-Arduino, have resulted in library version
incompatibilty between version 1.3x and version 2.x. 
Refer to the README file within the example subdirectory for details.
```
For a complete guide to getting started with PlatformIO and the RAKWireless WisBlock line of developer boards refer to the Helium documentation set at https://docs.helium.com/use-the-network/devices/development/rak-wisblock-starter.

NOTE: The WisBlock is not currently supported by PlatformIO out of the box. One must follow the guide referenced above when installing VSCode/PlatformIO for WisBlock.


## Resources
[Product Page](https://store.rakwireless.com/products/wisblock-starter-kit)  
[Manual](https://docs.rakwireless.com/Product-Categories/WisBlock/)  
[US Retailer - Parley Labs](https://shop.parleylabs.com)

## Firmware examples 
* [LoRaWan_OTAA](examples/LoRaWan_OTAA/)


### Software
The following products are required.

* [VSCode \(IDE)](https://code.visualstudio.com/)
    * [PlatformIO \(VScode Extension)](https://platformio.org/)
* [Helium Console](https://www.helium.com/console) 

### WisBlock Special Instructions
#### Antenna Type/location
The WisBlock starter kit comes with two antenna types, 
* the one that resembles an "I" is the LoRa antenna, this one connects to the connector on the core module marked LoRa, which is below the large K in the RAK logo.
* the one that resembles a "T" is the BLE antenna, this one connects to the connector on the core module marked BLE


