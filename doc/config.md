---
title: FPGA Configuration
layout: page
parent: FPGA Module
grand_parent: Hardware
nav_order: 2
---
# FPGA Configuration Modes

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
