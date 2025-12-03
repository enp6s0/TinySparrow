# TinySparrow
A compact, low-cost, CAN-FD enabled *core board* for all sorts of automotive shenanigans (and beyond)!

![TinySparrow X board](/docs/tsx-rendering.png?raw=true "TinySparrow X board rendering")

Ever wanted to integrate CAN bus functionality into your projects, but didn't want to
deal with laying out all the commonly used parts every single time?

Then TinySparrow is for you! Now in its 2nd generation, this cute little board combines a
[STM32G0X1](https://www.st.com/en/microcontrollers-microprocessors/stm32g0x1.html) MCU,
2x CAN-FD transceivers and power regulation all in a single board, ready to be integrated
in all your CAN-enabled device ideas.

### General specifications

* Compact footprint: `32 x 27 mm`

* QFN-48 **STM32G0x1** series ARM Cortex-M0+ microcontroller
	* Ships with [STM32G0B1CBU6](https://www.st.com/en/microcontrollers-microprocessors/stm32g0b1cb.html) by default (128K flash, 144K RAM)
	* Also compatible with [STM32G0C1CEU6](https://www.st.com/en/microcontrollers-microprocessors/stm32g0c1ce.html) should you want more RAM/flash or hardware crypto
	* Crystal-less USB device capability

* Dual CAN-FD (up to 5Mbps)
	* Texas Instruments [TCAN332G](https://www.ti.com/product/TCAN332G) PHYs
	* CAN bus ESD diodes included (probably a good idea to add another near connectors though)

* 2-stage automotive power supply
	* Much wider input range: 5 to 25 VDC in!
	* "Batteries included" protection: reverse polarity and voltage clamping diodes onboard
	* **3.3 VDC system voltage** (~500mA available for extra peripherals)
	* Texas Instruments [LMR43610-Q1](https://www.ti.com/product/LMR43610-Q1) buck converter (first stage)
	* STMicroelectronics [LD49100](https://www.st.com/resource/en/datasheet/ld49100.pdf) linear regulator (second stage)

* 2.54mm "pin grid array" I/O connectors
	* 72 total pins available, 61 currently used (all unused MCU pins available)
	* 11 pins reserved for future use (with other boards/revisions)
	* Easy to solder / design carrier boards for :)

### Module pinout

* Top left corner identified by golden notch
* Pins marked with `x` are reserved for future use (do not connect)

|              |              |             |        |        |        |        |     |     |     |            |            |
|:------------:|:------------:|:-----------:|:------:|:------:|:------:|:------:|:---:|:---:|:---:|:----------:|:----------:|
|      GND     |      GND     |  +VDC (in)  |    x   |    x   |    x   |    x   | GND |  x  |  x  |      x     |  GND       |
|     PA10     |  USB+ (PA12) | USB- (PA11) | CAN0 H | CAN0 L | CAN1 H | CAN1 L | GND |  x  |  x  |      x     | PB14       |
| nRESET (PF2) |  +3V3 (PROG) |             |        |        |        |        |     |     |     |    PB13    | PB12       |
| SWDIO (PA13) | SWCLK (PA14) |             |        |        |        |        |     |     |     |    PB11    | PB10       |
|      PD2     |     PA15     |             |        |        |        |        |     |     |     |     GND    |  PB2       |
|      PB3     |      PD3     |             |        |        |        |        |     |     |     |    PB15    |  PA8       |
|      PB4     |      PB5     |             |        |        |        |        |     |     |     |     PA9    |  PC6       |
|      PB6     |      PB7     |             |        |        |        |        |     |     |     | Power good |  PC7       |
|      PB8     |      PB9     |     PC13    |  PC15  |  +3V3  |   PF1  |   PA1  | PA3 | PA5 | PA7 |      x     |  +VDC (in) |
|      GND     |      GND     |     PC14    |  +VBAT |  +3V3  |   PF0  |   PA0  | PA2 | PA4 | PA6 |     GND    |  GND       |


### Revision/stepping info

* `A1`: initial release for Gen2 design
