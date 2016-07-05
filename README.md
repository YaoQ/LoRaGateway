# Low-cost LoRa Module
## Introduction

![](picture/lora.png)

This is low-cost LoRa gateway module which is powered by RFM96-low power long range transceiver module. The gateway can receive from any LoRa device and is designed to be fully customizable for a targeted application.Various applications are considered: water quality monitoring, cattle rustling, logistics and goods transportation.

This LoRa gateway could be qualified as "single connection" as it uses the SX1272, much like an end-device would do. However, in order to increase LoRa transmission robustness we improve the LoRa transmission with CSMA features (or so-called Listen Before Talk) and add Quality of Service guarantees with regards to radio time limitations. 

## Features

* LoRa Modem.
* 168 dB maximum link budget.
* +20 dBm - 100 mW constant RF output vs. V supply.
* +14 dBm high efficiency PA.
* Programmable bit rate up to 300 kbps.
* High sensitivity: down to -148 dBm.
* Bullet-proof front end: IIP3 = -12.5 dBm.
* Excellent blocking immunity.
* Low RX current of 10.3 mA, 200 nA register retention.
* Fully integrated synthesizer with a resolution of 61 Hz.
* FSK, GFSK, MSK, GMSK, LoRaTM and OOK modulation.
* Built-in bit synchronizer for clock recovery.
* Preamble detection.
* 127 dB Dynamic Range RSSI.
* Automatic RF Sense and CAD with ultra-fast AFC.
* Packet engine up to 256 bytes with CRC.
* Built-in temperature sensor and low battery indicator.

## Tutorials

### Prerequisites

**Hardware**

* Arduino UNO x 2
* Linker LoRa Radio x 2 
* Linker Base Shield x 2
* 4 Pin DuPont line x 4

**Software**

* Click [here](https://github.com/YaoQ/LoRaGateway) to download the Arduino project.
* Put the files in **src** folder which contains SX1272 libraries and examples into the directory of the Arduino IDE's libraries.

### Hardware assemble

* According to the following picture, connect LoRa module and Arduino Uno
**Note**: One is used to be LoRa gateway, and other one is used to be LoRa end device, they take same connections.
![](picture/hardware.png)


### LoRa Gateway 
* Open Arduino IDE
* **Open File --> Examples --> SX1272 --> Arduino_LoRa_Gateway**
* Upload code to Arduino Uno
**Note**: Please select the right serial port and board type.

![](picture/gatewaycode.png)

* Open the Arduino IDE Serial Monitor
* Set the baudrate as **38400**

![](picture/gatetest.png)

### LoRa end device

* Open other Arduino IDE window
* Open File --> Examples --> SX1272 --> Arduino_LoRa_temp
* Upload code to Arduino

![](picture/loratemp.png)

* Open the Arduino IDE Serial Monitor
* Set the baudrate as **38400**

![](picture/loratemptest.png)

### Check communication
* Open the two serial Monitor, one for LoRa_gateway and one for LoRa end device
* Restart both devices, then you can see them starting to communicate.

## Schematic
![](picture/sch.png)
