# TinySparrow

Tiny, low-cost, CAN-enabled core board for simple ECU designs!

![TinySparrow core board](/resources/SparrowCore.png?raw=true "TinySparrow core board")

Ever wanted to integrate CAN features into your ECU projects, but didn't want to deal with
building all the core parts (MCU/power/CAN PHY) all the time for every single one-off ECU?

Then TinySparrow is for you! This cute little board combines a [STM32F103TB](https://www.st.com/en/microcontrollers-microprocessors/stm32f103tb.html) MCU,
CAN transceiver, power regulation, and reverse polarity protection all in a single board, so it's ready
to be integrated in all your CAN-enabled device ideas.

### Bring your own X

To use TinySparrow in your project, simply create a carrier board and bring your own:

* Power source (+5 to +15V DC)
* Additional CAN bus ESD protection if needed (default transceiver is already ESD-rated for ±16 kV HBM, board is also TCAN332 compatible for even better protection)
* CAN termination (if needed)

For automotive applications, external load dump protection is **required** (TVS diode at a minimum).

NB: looking to put TinySparrow on a breadboard? [Here's an adapter for that!](https://github.com/enp6s0/TinySparrowBreadboardAdapter)
