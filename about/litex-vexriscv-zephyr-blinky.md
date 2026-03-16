---
title: LiteX and Zephyr OS blinky Demo
layout: page
parent: Technical Notes
nav_order: 2
---
# LiteX and Zephyr OS blinky Demo

This page describes steps to build LiteX SoC with VexRiscv CPU and run
Zephyr OS blinky demo on GMM-7550 module with USB 3 adapter and memory
modules.

## Building LiteX SoC

### Get LiteX board sources

```
git clone https://github.com/GMM-7550/litex-boards.git
cd litex-boards
git checkout gmm7550
```

### activate Python virtual environment with LiteX installed
```
. ~/Work/LiteX/bin/activate
```

### Build SoC
```
python ./litex_boards/targets/gmm7550_usb3.py --build --cpu-variant="standard" --with-async-ram
```

## Building Zephyr OS blinky Demo

Building Zephyr OS require the following tools to be installed and
properly configured:

- Zephyr OS sources (https://github.com/zephyrproject-rtos/zephyr)
  and RISC-V SDK
- `west` Zephyr's meta-tool (https://docs.zephyrproject.org/latest/develop/west/index.html)
- `uv` Python package and project manager (https://github.com/astral-sh/uv)

```
git clone https://github.com/GMM-7550/gmm7550-zephyr.git
cd gmm7550-zephyr
make
```

## Running blinky demo on GMM-7550

### Program FPGA configuration to the module

```
# Connect to the GMM-7550/RP2040 control CLI
~$ picocom -q -b 115200 /dev/ttyACM1

GMM-7550 Control CLI

Version    : 0.8.2
Git hash   : e34e7fd42ab86e61b12e2f9affaf41872b26d1c1
Build time : 2026-03-05 01:43:49

> on

> rst 1

> mux 2
SPI Mux configuration is 2

^A^X

~$ gmm7550_spi.py -c litex-boards/build/gmm7550/gateware/gmm7550.bit
```

### Running the demo

```
# Create a link to Zephyr OS blinky demo
~$ ln -s gmm7550-zephyr/build/zephyr/zephyr.bin

# Launch LiteX terminal -- it will start the board automatically
~$ litex_term --kernel ./zephyr.bin /dev/ttyACM0
...
```

<video>
<source src="https://github.com/GMM-7550/gmm-7550.github.io/raw/refs/heads/main/assets/videos/gmm7550-zephyr-blinky_2026-03-16.mp4">
</video>
