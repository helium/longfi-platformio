
This example uses the LSM6DSO sensor on the X-NUCLEO-IKS01A3 shield that is part of the Helium Developer Kit to detect "pedometer" events and relay them over the Helium Network.
```
Note: 
As mentioned within the source file for this project the LoRa runtime used by this project requires the
following for the network credential formats:

DEVEUI:  
// This EUI must be in little-endian format, so least-significant-byte first. When copying an EUI from 
// the Helium Console, this means to reverse the bytes.

APPEUI:  
// This should also be in little endian format, see above.

APPKEY:  
// This key should be in big endian format so most-significant-byte first. (or, since it is not really
// a number but a block of memory, endianness does not really apply). In practice, a key taken from
// the Helium Console can be copied as-is.
```

To emulate pedometer movement move the board horizontally in a cadence similar to a fast walk.
It will take a bit for the device to calibrate after the device is started.
