# TinySparrow
A compact, low-cost, CAN-FD enabled *core board* for all sorts of automotive shenanigans (and beyond)!

![TinySparrow X board](/docs/tsx-rendering.png?raw=true "TinySparrow X board rendering")

Ever wanted to integrate CAN bus functionality into your projects, but didn't want to
deal with laying out all the commonly used parts every single time?

Then TinySparrow is for you! Now in its 2nd generation, this cute little board combines a
[STM32G0B1CB](https://www.st.com/en/microcontrollers-microprocessors/stm32g0b1cb.html) MCU,
2x CAN-FD transceivers and power regulation all in a single board, ready to be integrated
in all your CAN-enabled device ideas.

### General specifications

* QFN-48 "STM32G0" series Cortex-M0 microcontroller
	* Ships with STM32G0B1CBU6 by default (128K flash, 144K RAM)
	* (should be) pin-compatible with the STM32G0C1CE should you want more RAM/flash or hardware crypto
	* Crystal-less USB device capability

* Dual CAN-FD (up to 5Mbps)
	* Texas Instruments [TCAN332G](https://www.ti.com/product/TCAN332G) PHYs
	* CAN bus ESD diodes included (probably a good idea to add another near connectors though)

* Dual stage power supply
	* 4 to 15 VDC in
	* Reverse polarity protection and voltage clamping diodes onboard
	* 3.3 VDC system voltage (~500mA available for off-board peripherals)
	* Texas Instruments [TPS629210-Q1](https://www.ti.com/product/TPS629210-Q1) buck converter (first stage)
	* STMicroelectronics [LD49100](https://www.st.com/resource/en/datasheet/ld49100.pdf) linear regulator (second stage)

* 2.54mm pin connectors
	* 72 total pins available, 60 currently used (all unused MCU pins available)
	* 12 pins reserved for future use (with other boards/revisions)
	* Easy to solder / design carrier boards for :)
