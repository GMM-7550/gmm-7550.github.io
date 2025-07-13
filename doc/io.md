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

Tables below show connections between FPGA I/O signals and module
connectors.

## Connector P1 (West)

| Signal | Pin | Pin | Signal |
| -----: | :-: | :-: | :----- |
|    GND   | 1 | 2 |    GND   |
| IO_WB_B1 | 3 | 4 | IO_WB_B0 |
| IO_WB_A1 | 5 | 6 | IO_WB_A0 |
|    GND   | 7 | 8 |    GND   |
| IO_WB_B2 | 9 | 10 | IO_WB_B3 |
| IO_WB_A2 | 11 | 12 | IO_WB_A3 |
|    GND   | 13 | 14 |    GND   |
| IO_WB_B4 | 15 | 16 | IO_WB_B5 |
| IO_WB_A4 | 17 | 18 | IO_WB_A5 |
|    GND   | 19 | 20 |    GND   |
| IO_WB_B6 | 21 | 22 | IO_WB_B7 |
| IO_WB_A6 | 23 | 24 | IO_WB_A7 |
|    GND   | 25 | 26 |    GND   |
| IO_WB_B8 | 27 | 28 | IO_WC_B0 |
| IO_WB_A8 | 29 | 30 | IO_WC_A0 |
| VIO_WB   | 31 | 32 | VIO_WB   |
| VCC25    | 33 | 34 | VCC25    |
| VIO_WC   | 35 | 36 | VIO_WC   |
| IO_WC_B1 | 37 | 38 | IO_WC_B3 |
| IO_WC_A1 | 39 | 40 | IO_WC_A3 |
|    GND   | 41 | 42 |    GND   |
| IO_WC_B2 | 43 | 44 | IO_WC_B5 |
| IO_WC_A2 | 45 | 46 | IO_WC_A5 |
|    GND   | 47 | 48 |    GND   |
| IO_WC_B4 | 49 | 50 | IO_WC_B8 |
| IO_WC_A4 | 51 | 52 | IO_WC_A8 |
|    GND   | 53 | 54 |    GND   |
| IO_WC_B6 | 55 | 56 | IO_WC_B7 |
| IO_WC_A6 | 57 | 58 | IO_WC_A7 |
|    GND   | 59 | 60 |    GND   |

## Connector P2 (North)

| Signal | Pin | Pin | Signal |
| -----: | :-: | :-: | :----- |
|    GND   | 1 | 2 |    GND   |
| IO_NA_B2 | 3 | 4 | IO_NA_B0 |
| IO_NA_A2 | 5 | 6 | IO_NA_A0 |
|    GND   | 7 | 8 |    GND   |
| IO_NA_B3 | 9 | 10 | IO_NA_B1 |
| IO_NA_A3 | 11 | 12 | IO_NA_A1 |
|    GND   | 13 | 14 |    GND   |
| IO_NA_B5 | 15 | 16 | IO_NA_B4 |
| IO_NA_A5 | 17 | 18 | IO_NA_A4 |
|    GND   | 19 | 20 |    GND   |
| IO_NA_B6 | 21 | 22 | IO_NA_B7 |
| IO_NA_A6 | 23 | 24 | IO_NA_A7 |
|    GND   | 25 | 26 |    GND   |
| IO_NA_B8 | 27 | 28 | IO_NB_B0 |
| IO_NA_A8 | 29 | 30 | IO_NB_A0 |
| VIO_NA   | 31 | 32 | VIO_NA   |
| VCC25    | 33 | 34 | VCC25    |
| VIO_NB   | 35 | 36 | VIO_NB   |
| IO_NB_B1 | 37 | 38 | IO_NB_B2 |
| IO_NB_A1 | 39 | 40 | IO_NB_A2 |
|    GND   | 41 | 42 |    GND   |
| IO_NB_B3 | 43 | 44 | IO_NB_B4 |
| IO_NB_A3 | 45 | 46 | IO_NB_A4 |
|    GND   | 47 | 48 |    GND   |
| IO_NB_B5 | 49 | 50 | IO_NB_B7 |
| IO_NB_A5 | 51 | 52 | IO_NB_A7 |
|    GND   | 53 | 54 |    GND   |
| IO_NB_B6 | 55 | 56 | IO_NB_B8 |
| IO_NB_A6 | 57 | 58 | IO_NB_A8 |
|    GND   | 59 | 60 |    GND   |

## Connector P3 (East)

| Signal | Pin | Pin | Signal |
| -----: | :-: | :-: | :----- |
|    GND   | 1 | 2 |    GND   |
| IO_EB_B7 | 3 | 4 | IO_EB_B8 |
| IO_EB_A7 | 5 | 6 | IO_EB_A8 |
|    GND   | 7 | 8 |    GND   |
| IO_EB_B5 | 9 | 10 | IO_EB_B4 |
| IO_EB_A5 | 11 | 12 | IO_EB_A4 |
|    GND   | 13 | 14 |    GND   |
| IO_EB_B6 | 15 | 16 | IO_EB_B2 |
| IO_EB_A6 | 17 | 18 | IO_EB_A2 |
|    GND   | 19 | 20 |    GND   |
| IO_EB_B3 | 21 | 22 | IO_EB_B0 |
| IO_EB_A3 | 23 | 24 | IO_EB_A0 |
|    GND   | 25 | 26 |    GND   |
| IO_EB_B1 | 27 | 28 | IO_EA_B7 |
| IO_EB_A1 | 29 | 30 | IO_EA_A7 |
| VIO_EB   | 31 | 32 | VIO_EB   |
| VCC25    | 33 | 34 | VCC25    |
| VIO_EA   | 35 | 36 | VIO_EA   |
| IO_EA_B8 | 37 | 38 | IO_EA_B4 |
| IO_EA_A8 | 39 | 40 | IO_EA_A4 |
|    GND   | 41 | 42 |    GND   |
| IO_EA_B6 | 43 | 44 | IO_EA_B2 |
| IO_EA_A6 | 45 | 46 | IO_EA_A2 |
|    GND   | 47 | 48 |    GND   |
| IO_EA_B5 | 49 | 50 | IO_EA_B1 |
| IO_EA_A5 | 51 | 52 | IO_EA_A1 |
|    GND   | 53 | 54 |    GND   |
| IO_EA_B3 | 55 | 56 | IO_EA_B0 |
| IO_EA_A3 | 57 | 58 | IO_EA_A0 |
|    GND   | 59 | 60 |    GND   |

## Connector P4 (South)

| Signal | Pin | Pin | Signal |
| -----: | :-: | :-: | :----- |
|    GND   | 1 | 2 |    GND   |
| IO_SB_B8 | 3 | 4 | IO_SB_B3 |
| IO_SB_A8 | 5 | 6 | IO_SB_A3 |
|    GND   | 7 | 8 |    GND   |
| IO_SB_B6 | 9 | 10 | IO_SB_B2 |
| IO_SB_A6 | 11 | 12 | IO_SB_A2 |
|    GND   | 13 | 14 |    GND   |
| IO_SB_B5 | 15 | 16 | IO_SB_B1 |
| IO_SB_A5 | 17 | 18 | IO_SB_A1 |
|    GND   | 19 | 20 |    GND   |
| IO_SB_B7 | 21 | 22 | IO_SB_B0 |
| IO_SB_A7 | 23 | 24 | IO_SB_A0 |
|    GND   | 25 | 26 |    GND   |
| IO_SB_B4 | 27 | 28 | IO_SA_B8 |
| IO_SB_A4 | 29 | 30 | IO_SA_A8 |
| VIO_SB   | 31 | 32 | VIO_SB   |
| VCC25    | 33 | 34 | VCC25    |
| VIO_SA   | 35 | 36 | VIO_SA   |
| IO_SA_B6 | 37 | 38 | IO_SA_B7 |
| IO_SA_A6 | 39 | 40 | IO_SA_A7 |
|    GND   | 41 | 42 |    GND   |
| IO_SA_B4 | 43 | 44 | IO_SA_B5 |
| IO_SA_A4 | 45 | 46 | IO_SA_A5 |
|    GND   | 47 | 48 |    GND   |
| IO_SA_B2 | 49 | 50 | IO_SA_B3 |
| IO_SA_A2 | 51 | 52 | IO_SA_A3 |
|    GND   | 53 | 54 |    GND   |
| IO_SA_B1 | 55 | 56 | IO_SA_B0 |
| IO_SA_A1 | 57 | 58 | IO_SA_A0 |
|    GND   | 59 | 60 |    GND   |
