
# Helium Basic Example

Here you will find a very basic example of a WisBlock/Helium embedded project that uses PlatformIO as the development IDE rather than the Arduino IDE.
This version will join the Helium network and periodically send a "Hello" to the Helium network.

## Support Library Version Incompatibility
Recent API changes to the runtime support library, SX126x-Arduino, have resulted in library version incompatibility between version 1.3x and version 2.x. The two major changes at the device application level are:
* The lmh_init() API requires 2 more parameters
* the device application is no longer required to call Radio.IrqProcess() within it's main processing loop.

The complete details of the version change can be found [here](https://github.com/beegee-tokyo/SX126x-Arduino/blob/master/README_V2.md).

The sample within this directory will support both version 1.3.x and version 2.x of the SX126x-Arduino. The platformio.ini contains the following snippet:
```
;; comment out the following if using Version 1.3.x of
;; the SX126x-Arduino library
lib_deps = beegee-tokyo/SX126x-Arduino   ; version 2

;; Uncomment the following 2 lines if using Version 1.3.x of
;; the SX126x-Arduino library
;lib_deps = beegee-tokyo/SX126x-Arduino@^1.2.1  ; version 1.3.x
;build_flags = -DREGION_US915 -DSX126x_Arduino_Ver1  ; version 1.3.x
```

The above is configured to support compiling against version 2.x of the SX126x-Arduino library. 

Based on the value of lib_deps, PlatformIO will download the appropriate library version into the project's .pio/libdeps/wiscore_rak4631 subdirectory. This can be verified by inspecting the library.properties file that is contained within the downloaded library.

The device application's main.cpp file contains the following conditional compile directive with determines which version of API to call.
```
#ifdef SX126x_Arduino_Ver1
``

### Hardware
The only hardware required is:
* the [WisBlock Starter Kit](https://store.rakwireless.com/products/wisblock-starter-kit) containing  the base board with the core module installed.
* one USB 2.0 A-Male to Micro B interface cable.

#### Antenna Type/location
The WisBlock starter kit comes with two antenna types, 
* the one that resembles an "I" is the LoRa antenna, this one connects to the connector on the core moduke marked LoRa, which is below the large K in the RAK logo.
* the one that resembles a "T" is the BLE antenna, this one connects to the connector on the core module marked BLE


