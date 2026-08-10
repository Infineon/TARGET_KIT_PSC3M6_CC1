# KIT_PSC3M6_CC1 BSP Release Notes
The PSOC™ Control C3M6 Digital Power Control Card (KIT_PSC3M6_CC1) is based on the Infineon PSOC™ Control C3M6 microcontroller and features an onboard debugger along with a 120-pin edge connector for seamless integration with compatible power boards. Powered by an Arm® Cortex®-M33 based PSOC™ Control MCU, the card is designed to evaluate, develop, and demonstrate advanced digital power control applications. When paired with supported power boards, it showcases the capabilities of the PSOC™ Control C3M6 device for power conversion, motor control, and other real-time power stage control applications. The card plugs into a standard 120-pin edge connector, providing a flexible platform for rapid prototyping, system evaluation, and application development using the PSOC™ Control C3M6 MCU.

**Note:** Programming this kit requires installing [SEGGER J-Link software](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack).


### What's Included?
The KIT_PSC3M6_CC1 library includes the following:
* BSP specific makefile to configure the build process for the board
* cybsp.c/h files to initialize the board and any system peripherals
* cybsp_types.h file describing basic board setup
* CM33 Linker script & startup code for GCC toolchain
* Configurator design files (and generated code) to setup board specific peripherals
* .lib file references for all dependent libraries
* API documentation

### What Changed?
#### v0.5.0
* Initial pre-production release

### Supported Software and Tools
This version of the KIT_PSC3M6_CC1 BSP was validated for compatibility with the following Software and Tools:

| Software and Tools                        | Version |
| :---                                      | :----:  |
| ModusToolbox™ Software Environment        | 3.8.0   |
| GCC Compiler                              | 14.2.1  |

Minimum required ModusToolbox™ Software Environment: v3.6.0

### More information
* [KIT_PSC3M6_CC1 BSP API Reference Manual][api]
* [KIT_PSC3M6_CC1 Documentation](https://www.infineon.com/evaluation-board/KIT-PSC3M6-CC1)
* [Infineon Technologies AG](https://www.infineon.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.infineon.com/modustoolbox)

[api]: https://infineon.github.io/TARGET_KIT_PSC3M6_CC1/html/modules.html

---
© 2026, Infineon Technologies AG, or an affiliate of Infineon Technologies AG.