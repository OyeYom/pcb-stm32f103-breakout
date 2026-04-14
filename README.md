# STM32F103 Microcontroller PCB

> A custom printed circuit board for the STM32F103C8T6 microcontroller, 
> designed as a development/breakout board with onboard power regulation, 
> USB connectivity, and full GPIO header access.

![PCB 3D View](images/3d-top.png)

## Overview
This board was designed to provide a ready-to-use platform for the STM32F103C8T6 
microcontroller. Instead of relying on off-the-shelf development boards, this custom 
PCB was laid out from scratch in Altium Designer — covering everything from schematic 
capture to Gerber output.

The board includes onboard 5V→3.3V regulation, a micro USB connector for programming, 
dual 20x1 GPIO breakout headers, an SWD debug interface, reset button, and status LEDs.

## Key Features
- STM32F103C8T6 (32-bit ARM Cortex-M3, 72MHz)
- Onboard 5V to 3.3V regulation via RT9193-33GB LDO
- Micro USB connector for power and programming
- Dual 20x1 Bergstrip headers exposing all GPIO pins
- 2x3 SWD debug/programming header
- 8MHz HSE crystal + 32.768KHz LSE crystal for RTC
- Tact switch for RESET and BOOT mode selection
- Power indicator LED (Red)
- 2-layer PCB, board size: 53.34mm × 22.86mm

## Tools Used
- Altium Designer (schematic capture, PCB layout, 3D render, Gerber output)

## Board Specifications
| Parameter | Value |
|---|---|
| Dimensions | 53.34mm × 22.86mm |
| Layers | 2 |
| MCU | STM32F103C8T6 (LQFP-48) |
| Supply Voltage | 5V via USB |
| Logic Voltage | 3.3V |
| Crystal (HSE) | 8MHz |
| Crystal (LSE) | 32.768KHz |
| Programmer Interface | SWD (2x3 header) |

## Components Used
- STM32F103C8T6 Microcontroller
- RT9193-33GB LDO Voltage Regulator (5V → 3.3V)
- Capacitors: 0.1µF, 1µF, 22pF
- Resistors: 1kΩ, 10kΩ
- Crystal Oscillators: 8MHz, 32.768KHz
- Micro USB 2.0 Connector
- 20x1 Bergstrip Headers (×2)
- 2x3 Bergstrip Header (SWD)
- Tact Switch
- Red SMD LEDs

## Schematic
![Schematic](images/schematic.png)

## PCB Layout
![Top Layer](images/top-layer.png)
![Bottom Layer](images/bottom-layer.png)

## 3D Render
![3D Top](images/3d-top.png)
![3D Bottom](images/3d-bottom.png)

## Design Process
1. Created component symbols and footprints in Altium library
2. Captured full schematic across 2 sheets
3. Imported netlist to PCB document
4. Sized board to 53.34mm × 22.86mm
5. Placed components and routed tracks manually
6. Applied ground polygon pour on both layers
7. Generated Gerber output files for fabrication

## What I Learned
- Full PCB design workflow in Altium Designer from scratch
- Proper decoupling capacitor placement for STM32 power pins
- SWD interface wiring for STM32 programming and debugging
- Managing multi-sheet schematics and netlists
- Generating fabrication-ready Gerber output files
