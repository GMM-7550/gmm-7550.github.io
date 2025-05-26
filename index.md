---
layout: home
---
<img src="{{ "/assets/images/fpga-gmm7550.png" | relative_url }}" align="center">

The GMM-7550 is a module providing a convenient way to evaluate
[GateMate
FPGA](https://colognechip.com/programmable-logic/gatemate/){:target="_blank"}
from Cologne&nbsp;Chip&nbsp;AG and to build custom systems around it.
This site contains the documentation for the GMM-7550 module, accompany boards,
configuration and control software, and FPGA design examples.

All the hardware design data, software, and RTL code are released
under free and permissive licenses ([CERN OHL-P
2.0](https://spdx.org/licenses/CERN-OHL-P-2.0.html) and
[MIT](https://spdx.org/licenses/MIT)) and can be accessed
at the project [GitHub repositories](https://github.com/GMM-7550).

The module consists of the FPGA (CCGM1A1) in BGA324 15x15&nbsp;mm
package, power converters, reset, clocking and configuration support
circuitries.

To evaluate the module, program the PLL configuration EEPROM and
configuration SPI-NOR FLASH on the module either of three adapters may
be used:

- Raspberry Pi HAT adater (connected to 40-pin GPIO of any Raspberry
  Pi SBC)
- RP2040 USB adapber (under development)
- an adapter board with experimental USB&nbsp;3 interface
  (also including RP2040 for configuration and control)

A memory extension module auguments the GMM-7550 with external SRAM
and additiona SPI-NOR FLASH for software development with a soft-core
CPU or SoC implemented inside the FPGA.

An IO Breakout board (under development) provides a convenient way to access FPGA IO
signals available on the GMM-7550 IO Connectors.
