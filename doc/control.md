---
title: Module Control
layout: page
parent: FPGA Module
grand_parent: Hardware
nav_order: 1
---
# FPGA Module Control Interfaces

The GMM-7550 module is controlled by several discrete signals and via
I2C bus. An FPGA on the module may be configured via JTAG or SPI
interface, and an SPI NOR FLASH on the module is accessible via the
same SPI bus.

The table below shows the GMM-7550 module control signals available on
the P5 connector, and the following subsections provides more details
on each interface and control signal.

## P5 Connector

| Signal | Pin | Pin | Signal |
| -----: | :-: | :-: | :----- |
|    GND   | 1 | 2 |    GND   |
| CLK3_N | 3 | 4 | IO_WB_B0 |
| CLK3_P | 5 | 6 | IO_WB_A0 |
|    GND   | 7 | 8 |    GND   |
| +2.5V | 9 | 10 | +2.5V |
| CLK2_N   | 11 | 12 | rfu |
| CLK2_P   | 13 | 14 |  rfu   |
|    GND | 15 | 16 | GND |
| SER_RX_P | 17 | 18 | SER_TX_P |
| SER_RX_N | 19 | 20 | SER_TX_N |
|    GND | 21 | 22 | GND |
|   CLK0 | 23 | 24 | SDA |
|    GND | 25 | 26 | SCL |
| SPI_CLK | 27 | 28 | GND |
| SPI_D0 | 29 | 30 | SPI_CS_N |
| SPI_D2 | 31 | 32 | SPI_D1   |
| SPI_D3 | 33 | 34 | SPI_FWD  |
| CFG_FAILED_N | 35 | 36 | CFG_DONE |
| GND | 37 | 38 | GND |
| JTAG_TDI | 39 | 40 | JTAG_TDO |
| JTAG_TCK | 41 | 42 | JTAG_TMS |
| GND | 43 | 44 | GND |
| +2.5V | 45 | 46 | RSTO_N |
| OFF_N | 47 | 48 | MR_N |
| GND | 49 | 50 | GND |
| Vin | 51 | 52 | Vin |
| Vin | 53 | 54 | Vin |
| Vin | 55 | 56 | Vin |
| Vin | 57 | 58 | Vin |
| Vin | 59 | 60 | Vin |

## Input Power

Vin

## Discrete Control Signals

MR_N
OFF_N
RSTO_N

## JTAG Interface (FPGA Configuration)

## SPI

### SPI Switch

## I2C Interface

- Clock PLL
- I2C GPIO: FPGA configuration mode and SPI switch control

## Transceiver Signals

## Input and Output Clock Signals
