---
title: FPGA Module
layout: page
parent: Hardware
has_children: true
nav_order: 1
---
# FPGA Module

|Top Side|Bottom Side|
|:-:|:-:|
|![Top Side]( {{ "/assets/images/gmm7550-top.png" | relative_url }} )|![Bottom Side]( {{ "/assets/images/gmm7550-bottom.png" | relative_url }} ) |
|<img src="{{ "/assets/images/gmm7550.jpg" | relative_url }}" width="65%" style="transform:rotate(90deg);">|![Bottom Side]( {{ "/assets/images/gmm7550-bottom.jpg" | relative_url }} ) |

## Cologne Chip GateMate FPGA

The module is based on the CCGM1A1 GateMate FPGA in
BGA324 15x15 mm package. The FPGA provides:

- 20,480 programmable elements for combinatorial and sequential logic
- 20,480 8-input LUT-trees / 40,960 4-input LUT-trees
- 40,960 Latches / Flip-flops within programmable elements
- each programmable element configurable as:
  * 1-bit full adder
  * 2-bit full adder or
  * 2x2-bit multiplier
- dedicated logic and routing for fast arithmetic and arbitrary-sized multipliers
- 9 general purpose input / output (GPIO) banks (8 available on the GMM-7550 module connectors)
  * 162 user-configurable GPIOs (144 available on the module connectors)
  * all GPIOs configurable as single-ended or LVDS differential pairs
  * double data rate (DDR) registers in I/O cells
  * I/O voltage range from 1.2 to 2.5 V
- 4 clock generators (PLL)
  * maximum PLL output frequency from 250 MHz to 416.75 MHz
- 5 Gb/s serializer / deserializer (SerDes)
- flexible memory resources
  * 1,310,720 total RAM bits distributed over 32 SRAM blocks
  * each RAM block configurable as two independent 20 Kbit blocks or single 40 Kbit block
  * simple or True Dual Port (SDP / TDP) or FIFO mode
  * data width from 1 bit up to 40 bits (TDP) or 80 bits (SDP)
  * bit-wide write enable
  * error checking and correcting (ECC) for certain bit widths
- flexible device configuration
- application modes: *low power*, *economy*, *speed* (selectable with a solder jumpers on the module)
- 15x15 mm 324 balls 0.8 mm fine pitch Ball Grid Array (FBGA) package

## Input Power and Converters

The module is powered from a single power supply in **2.9 to 6.5&nbsp;V**
range, so it may be powered directly from a commodity 3.3 or
5&nbsp;V power supply or a single Li-Pol cell.

On the module high-efficiency DC-DC converters generate the FPGA core
supply voltage (hardware configurable to 0.9, 1.0, or 1.1&nbsp;V), I/O
voltage for the configuration interface, SPI-NOR FLASH, clock
generator, and I/O banks (fixed at 2.5&nbsp;V). The 2.5&nbsp;V are
provided on the module connectors to power a base board components.

Additional low-noise LDO regulator is provided for the FPGA high-speed
serial transceiver and PLLs (hardware configurable 1.0 or 1.1&nbsp;V).

The DC-DC convertes on the module are synchronized with the main
module clock to reduce power supplies noise level. The converters
operate at 1.25&nbsp;MHz with a 180 degree phase shift to reduce
inducted ripple on the input power feed.

## Clock Generator

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

## FPGA Configuration

The module supports all the GateMate FPGA configuration modes:

- SPI Active Mode from the on-module SPI-NOR FLASH (default)
- SPI Active Mode from an SPI-NOR on a base board
- SPI Passive Mode with an external SPI master
- JTAG Mode

The configuration mode and SPI multiplexing are controlled via 16-bin
I2C-bus I/O port on the module.

The on-module SPI-NOR FLASH may be accessed and programmed via SPI
interface from a base board or via the FPGA JTAG interface.

An I/O voltage for the module control (I2C) and configuration
interfaces (JTAG and SPI) is fixed at 2.5&nbsp;V.

## FPGA General Purpose Input-Output Signals

XCThe CCGM1A1 FPGA provides up to 162 general purpose input/output
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
