---
title: Clocks
layout: page
parent: FPGA Module
grand_parent: Hardware
nav_order: 3
---
# Module Clocks and PLLs

The GMM-7550 module includes Texas Instruments CDCE6214 clock
generator with one PLL. A clock reference is provided by a 25&nbsp;MHz
crystal on the module. If a higher precision, stability, or a
synchronization to an external reference is required, an LVDS clock
input may be used as a primary reference for the PLL.

The generator provides 100&nbsp;MHz reference clock to the FPGA SerDes
PLL, reference 25&nbsp;MHz (CMOS) and two programmale (LVDS) outputs
on the module connector and a clock signal for DC-DC synchronization.

The generator has internal configuration EEPROM and is programmable
via I2C interface.

The FPGA input clock signals CLK0..3 are available on the general
purpose input-output bank SB (South B) signals on the module
connector. Additionally, SPI and JTAG clock signals may be used for
user's logic synchronization inside the FPGA.
