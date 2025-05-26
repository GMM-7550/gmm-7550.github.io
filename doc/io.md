---
title: FPGA I/O
layout: page
parent: FPGA Module
grand_parent: Hardware
nav_order: 5
---
# FPGA Input/Output Signals

The CCGM1A1 FPGA provides up to 162 general purpose input/output
signals split into 9 banks (with 18 single-ended signals or 9 LVDS
pairs each) with independent power supplies. 144 FPGA's general
purpose input-output signals (8 banks) are available on 4 module
connectors. Input-output voltage from 1.2 to 2.5&nbsp;V for each of
the 8 I/O banks may be independetnly supplied from a base board or from
a power converter on the module (fixed at 2.5&nbsp;V, default hardware
option).

An input/output bank WA (West A) signals are used on the module for
configuration mode selection, SPI and JTAG interfaces, control and
status signals and are not available for general use. The I/O voltage
of the WA bank is fixed on the module at 2.5&nbsp;V.
