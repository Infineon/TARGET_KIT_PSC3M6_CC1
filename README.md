# KIT_PSC3M6_CC1 BSP

## Overview

The PSOC™ Control C3M6 Digital Power Control Card (KIT_PSC3M6_CC1) is based on the Infineon PSOC™ Control C3M6 microcontroller and features an onboard debugger along with a 120-pin edge connector for seamless integration with compatible power boards. Powered by an Arm® Cortex®-M33 based PSOC™ Control MCU, the card is designed to evaluate, develop, and demonstrate advanced digital power control applications. When paired with supported power boards, it showcases the capabilities of the PSOC™ Control C3M6 device for power conversion, motor control, and other real-time power stage control applications. The card plugs into a standard 120-pin edge connector, providing a flexible platform for rapid prototyping, system evaluation, and application development using the PSOC™ Control C3M6 MCU.

**Note:** Programming this kit requires installing [SEGGER J-Link software](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack).


![](docs/html/board.png)

To use code from the BSP, simply include a reference to `cybsp.h`.

## Features


Kit Features:

- PSOC™ Control C3M6 (Arm® Cortex®-M33 based) Microcontroller
- 120-pin edge connector exposing all PSOC™ Control C3M6 IOs
- On-board XMC4200 debug probe (J-Link) with isolated USB Type-C interface supporting SWD
- Isolated UART virtual COM port and isolated CAN FD transceiver interface
- Isolated 5 V power supply with 5 V-to-3.3 V LDOs
- One status LED, a reset button, and an I2C header


Kit Contents:

- PSOC™ Control C3P6 Digital Power Control Card
- PSOC™ Control C3P6 Interface Board
- Type C to USB A cable


## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the KIT_PSC3M6_CC1.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default in some BSPs, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.  Newer BSPs pull in the v3.x HAL, which enables itself via its own makefile, so CY_USING_HAL is not present.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.

### Clock Configuration

|  Clock  |   Source  | Output Frequency |
| :-----: | :-------: | :--------------: |
|   FLL   |    IHO    |    100.0 MHz     |
| CLK_HF0 | CLK_PATH1 |     180 MHz      |
| CLK_HF1 | CLK_PATH1 |     180 MHz      |
| CLK_HF2 | CLK_PATH0 |     100 MHz      |
| CLK_HF3 | CLK_PATH0 |      50 MHz      |
| CLK_HF4 | CLK_PATH1 |     180 MHz      |

### Power Configuration

* System Active Power Mode: OD
* System Idle Power Mode: CPU Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The KIT_PSC3M6_CC1 Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [KIT_PSC3M6_CC1 BSP API Reference Manual][api]
* [KIT_PSC3M6_CC1 Documentation](https://www.infineon.com/evaluation-board/KIT-PSC3M6-CC1)
* [Infineon Technologies AG](https://www.infineon.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.infineon.com/modustoolbox)

[api]: https://infineon.github.io/TARGET_KIT_PSC3M6_CC1/html/modules.html
[settings]: https://infineon.github.io/TARGET_KIT_PSC3M6_CC1/html/md_bsp_settings.html

---
© 2026, Infineon Technologies AG, or an affiliate of Infineon Technologies AG.