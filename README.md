# electriQ-ESPHome

## Background

I bought a number of these electriQ minisplit air conditioners and they work fine with the in-built wifi module and its Tuya integration into Home Assistant.  But I prefer to use on-premises solutions that don't rely on cloud, especially when that cloud is Chinese owned. A bit of reverse engineering of the Tuya datapoints led to this design.

The electriQ brand is, as far as I can tell, a UK specific brand that is put onto more generic Chinese products.  If your board looks like these then it might also work.

Front of the original board:
![alt text](https://github.com/PhilTheGeek/electriq-ESPHome/blob/main/pictures/Original%20Board%20Front.jpeg?raw=true)

Back of the original board:
![alt text](https://github.com/PhilTheGeek/electriq-ESPHome/blob/main/pictures/Original%20Board%20Back.jpeg?raw=true)

## Bill of Materials

| Part | Part Number |
| ---- | ----------- |
| R1 | 10k 0603 |
| R2 | 10k 0603 |
| R3 | 100R 0603 |
| R4 | 10k 0603 |
| R5 | 10k 0603 |
| R6 | 100R 0603 |
| U1 | ESP32-C3 SuperMini (must be one with onboard flash)|
| J1 | S4B-PH-K-S |

## ESPHome

Use the example YAML, amending entries with {} tags.  If your unit has horizontal swing then uncomment the 107 datapoint. 
There are 3 bitmask bytes which I've left in. I've never seen them change. Data point 108 is always 0xFF, 109 0x00 and 110 0x00.  Please let me know if you find out if they change and why.

## New board

Gerbers in the gerber folder and the board will end up looking a bit like this (I've rotated Q2 and R4 to align with the other components since building this board).

![alt text](https://github.com/PhilTheGeek/electriq-ESPHome/blob/main/pictures/Board%20Front.jpeg?raw=true)


