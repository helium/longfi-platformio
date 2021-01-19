
# Helium Basic Example

This is a very basic example of a CubCell to Helium embedded project that uses PlatformIO as the development IDE rather than the Arduino IDE.
This version will join the Helium network and periodic send a 4 byte message to the Helium network.

A quick start guide that can be used along with this sample can be found [here](../../../getting-started.md).

Sample/target deivce specific details if any can be found below.

#### Upload caution
```
Prior to attempting to upload your binary make sure any terminal session that might be attached 
to the debug comm port has been closed/deleted. Occasionally but not always, PlatformIO will automatically
close the comm port. If it does not close the port upload errors will occur.
```

