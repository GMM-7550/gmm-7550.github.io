---
title: openFPGALoader
layout: page
parent: Control Software
nav_order: 3
---
# openFPGALoader and dirtyJtag

RP2040 firmware implements dirtyJtag protocol and may be used with
`openFPGALoader` to configure FPGA and program configuration SPI NOR
on the module.

## Set FPGA Configuration Mode to JTAG

```
picocom -q -b 115200 /dev/ttyACM1


GMM-7550 Control CLI

Version    : 0.8.3
Git hash   : 641a52c9a9bc8b57c1e6805055b0ecd6225f0566
Build time : 2026-03-17 17:37:47

> on

> cfg c
Configuration mode is c
```

## Verify Access to the FPGA

Check USB-to-JTAG adapter is present.

```
$ openFPGALoader --scan-usb
empty
Bus device vid:pid       probe_type manufacturer     serial           product
001 058    0x1209:0xc0ca dirtyJtag  GMM-7550 Project FFFFFFFFFFFFFFFF USB3 Adapter Board
```

Check a scan chain and identify connected device

```
$ openFPGALoader --cable dirtyJtag --detect --freq 15000000
empty
Jtag frequency : requested 15000000Hz -> real 15000000Hz
index 0:
	idcode 0x20000001
	manufacturer colognechip
	family GateMate Series
	model  GM1Ax
	irlength 6
```

## Configure FPGA

```
$ openFPGALoader --cable dirtyJtag --freq 15000000 --bitstream gmm7550_standard_2026-03-07.bit
empty
Jtag frequency : requested 15000000Hz -> real 15000000Hz
Load SRAM via JTAG: [==================================================] 100.00%
Done
```

## Program Configuration SPI NOR

```
$ openFPGALoader --cable dirtyJtag --freq 15000000 -f gmm7550_standard_2026-03-07.bit
empty
write to flash
Jtag frequency : requested 15000000Hz -> real 15000000Hz
JEDEC ID: 0x9d6016
Detected: ISSI IS25LP032 64 sectors size: 32Mb
00000000 00000000 00000000 00
start addr: 00000000, end_addr: 000a0000
Erasing: [==================================================] 100.00%
Done
Writing: [==================================================] 100.00%
Done
```
