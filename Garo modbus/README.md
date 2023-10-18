# Garo energy meter

This configuration file is an example of how to retrieve data from a Garo energy meter 

## Component
* A Raspberry Pico W  
* DollaTek TTL to RS485 [Amazon](https://www.amazon.se/DollaTek-RS485-adapter-seriell-niv%C3%A5omvandlare/dp/B07DJ4TGY3)  
* Garo [GNM3D-RS485](https://www.garo.se/sv/produkter/energimatare/energimatare-3-fas-direktmatare/energimatare-3f-modb-rs485), can find documentation about the protocol.
* Esphome

## Wiring:  
Pico to DollaTek  
GPIO00 - pin 1 - UART TX pin on Pico  
GPIO01 - pin 2 - UART RX pin on Pico  

DollaTek to Garo    
A + -> Garo B+ (8)  
B - -> Garo A- (9)  
Third (GND) -> Garo GND (10)  

## 
It does not read all data that is available in the meter but adding more should be fairly simple. 
 
Tried to optimize the reading of registers but Im not sure if its the best way to do it.

