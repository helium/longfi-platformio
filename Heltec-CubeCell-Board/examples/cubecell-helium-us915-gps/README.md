
# Helium Basic Example

This is an example of a CubCell to Helium embedded project that uses PlatformIO as the development IDE rather than the Arduino IDE.
This version will join the Helium network, attempt to acquire a GPS signal lock, then send periodic message containing those coordinates to the Helium network. If a GPS lock is not successful the message coordinates will contain all 0s.
