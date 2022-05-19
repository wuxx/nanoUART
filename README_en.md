# nanoUART User Manual
* [Introduce](#Introduce) 
* [Feature](#Feature) 
* [Pin Definition](#pin-definition)
* [How to Use](#how-to-use)
    * [Wire Connection](#wire-connection)
	* [IO Level Change](#io-level-change)
	* [Serial Software](#serial-software)
* [FAQ](#faq)
	
# Introduce
nanoUART is a serial tool with TYPE-C interface build by MuseLab. The size is 2.2cmx1.7cm. It can support up to 6Mbps baud rate communication, support flow control, and support multiple Various level IO, including 5V/3.3V/2.5V/1.8V and user-defined level VREF input.

<div align=center>
<img src="https://github.com/wuxx/nanoUART/blob/master/doc/nanoUART-top.jpg" width = "500" alt="" align=center />
<img src="https://github.com/wuxx/nanoUART/blob/master/doc/nanoUART-bottom.jpg" width = "530" alt="" align=center />
</div>

# Feature
- Hardware full duplex, supports up to 6Mbps baud rate communication
- Support RTS/CTS hardware flow control, support common MODEM communication signals
- Support a variety of IO levels
- TYPE-C interface, small size, easy to use

## Pin Definition
Top|Bottom |
----|---- |
GND | RI  | 
TX  | CTS |
RX  | DSR |
DTR | DCD |
RTS | VREF|
3V3 | 5V  |

Note 1: Provide 5V/3.3V, 5V power supply current up to 500mA, 3.3V output current up to 300mA  
Note 2: VREF is the external reference pin level input


# How to Use

## Wire Connection
nanoUART|MCU |
----|----|
GND | GND | 
TX | RX  |
RX | TX  |

## IO Level Change
The IO reference level can be selected by the short-circuit bridge on the back of the nanoUART. By default, four IO levels are provided internally, 5V/3.3V/2.5V/1.8V. You can also short-circuit VREF and provide reference through the external VREF pin


## Serial Software
recommended to use sscom or putty (under the doc directory)
![sscom](https://github.com/wuxx/nanoUART/blob/master/doc/sscom.png)

# FAQ
