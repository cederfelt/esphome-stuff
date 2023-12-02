# Garo energy meter

This configuration file is an example of how to retrieve data from a Garo energy meter 

## Components
* A Raspberry Pico W  
* DollaTek TTL to RS485 [Amazon](https://www.amazon.se/DollaTek-RS485-adapter-seriell-niv%C3%A5omvandlare/dp/B07DJ4TGY3)  
* Garo [GNM3D-RS485](https://www.garo.se/sv/produkter/energimatare/energimatare-3-fas-direktmatare/energimatare-3f-modb-rs485), can find documentation about the protocol.
* Esphome

## Wiring
How to wire, other pins with the same functionality can of course be used instead.   
pico pinout https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf  

| GPIO | Pin number |Description | DollaTek RS485 Pin |
|-|-|-|-|
| 00 | 1 | UART TX | TXD |
| 01 | 2 | UART RX | RXD |
| - | 36 | 3_3 | VCC |
| - | 38 | GND | GND |

| DollaTek RS495 Pin | Garo pin name | Garo Pin number|
|-|-|-|
| A+ | B+ | 8 |
| B- | A- | 9 |
| GND | GND | 10 |

## Notes
It does not read all data that is available in the meter but adding more should be fairly simple. 
 
Tried to optimize the reading of registers but Im not sure if its the best way to do it.

