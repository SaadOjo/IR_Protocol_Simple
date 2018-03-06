# IR_Protocol_Simple
A simplified protocol to transmit and receive signals over infrared medium. 

The Library is intended to be used in time critical systems where the programmer can not afford to lock hardware resources. 
An example of such a system can be a realtime controller used in drones where basic commands signals need to be identified.

## IR Transmitter Library

Initialise with pin number 9 or 10
```
infraredTransmitter myTransmitter(9);
myTransmitter.setSignalIdentity(2); //Performs hardware configurations
```
to set the signal type to be transmitted:
```
myTransmitter.setSignalIdentity(2);
```
to transmit the signal:

Please note that the accuracy of the signal timings depend on the time period of the loop. 
```
myTransmitter.transmit(); // Should be called every loop
```
to turn on the led:
```
myTransmitter.alwaysOn(); // Only needs to be called once
```
## IR Receiver Library

Initialise on any digital pin.
```
infraredReciever myReciever(2);
myReciever.init();
```
to detect the signal:
```
myReciever.detect(); // must be called on each loop
```
detect functions returns 0 when no signal is detected
returns non zero values for other signal types



