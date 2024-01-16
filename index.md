---
layout: home
---
<img src="{{ "/assets/images/gmm7550.jpg" | relative_url }}" align="right" width="30%">

The GMM-7550 is a small module providing a convenient way to evaluate
[GateMate
FPGA](https://colognechip.com/programmable-logic/gatemate/){:target="_blank"}
from Cologne&nbsp;Chip&nbsp;AG.  This site provides the documentation
for the GMM-7550 module, accompany boards, configuration and control
software, and FPGA design examples.

The module consists of the FPGA (CCGM1A1) in BGA324 15x15&nbsp;mm
package, power converters, reset, clocking and configuration support
circuitries.

To evaluate the module, program the PLL configuration EEPROM and
configuration SPI-NOR FLASH on the module either of two adapters may
be used:

- Raspberry Pi HAT adater (connected to 40-pin GPIO of any Raspberry
  Pi SBC)
- RP2040 USB adapber

A memory extension module auguments the GMM-7550 with external SRAM
and additiona SPI-NOR FLASH for software development with a soft-core
CPU or SoC implemented inside the FPGA.

An IO Breakout board provides a convenient way to access FPGA IO
signals available on the GMM-7550 IO Connectors.
