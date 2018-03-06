# IR_Protocol_Simple
A simplified protocol to transmit and receive signals over infrared medium

# IR Transmitter Library

Initialise with pin number 9 or 10

infraredTransmitter myTransmitter(9);
myTransmitter.setSignalIdentity(2); //Performs hardware configurations

to set the signal type to be transmitted:-

myTransmitter.setSignalIdentity(2);

to transmit the signal:

Please note that the accuracy of the signal timings depend on the time period of the loop. 

myTransmitter.transmit(); // Should be called every loop

to turn on the led:

myTransmitter.alwaysOn(); // Only needs to be called once

# IR Transmitter Library

Initialise on any digital pin

infraredReciever myReciever(2);
myReciever.init();

to detect the signal

myReciever.detect(); // must be called on each loop

detect functions returns 0 when no signal is detected
returns non zero values for other signal types



