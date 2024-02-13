---
title: Raspberry Pi HAT Adapter
layout: page
parent: Hardware
nav_order: 2
---
# Raspberry Pi HAT Adapter

|KiCad 3D|Assembled HAT|
|:-:|:-:|
|![KiCad 3D]( {{ "/assets/images/hat-gmm7550.png" | relative_url }} )|![Assembled HAT]( {{ "/assets/images/hat-gmm7550.jpg" | relative_url }} ) |

- attaches to a Raspberry-Pi compatible 40-pin I/O header
- makes use of GPIOs, 2x I2C-bus, and SPI
- GMM-7550 module may be powered either with 5&nbsp;V from the 40-pin
  header or from a dedicated power connector
- power control and current consumption monitoring of the GMM-7550
  module with Analog Devices ADM1177
- reset signal control to the module
- LEDs indicating the module power, reset and configuration status
- voltage level translators for I2C-bus, SPI, and GPIOs
- CAT24C32 HAT ID EEPROM with write protection
- 10-pin JTAG programming connector
- two 12-pin Pmod connectors with 3.3&nbsp;V I/O signals
