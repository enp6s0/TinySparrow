# TinySparrow

Tiny, low-cost, CAN-enabled core board for simple ECU designs!

![TinySparrow core board](/resources/SparrowCore.png?raw=true "TinySparrow core board")

Ever wanted to integrate CAN features into your ECU projects, but didn't want to deal with
building all the core parts (MCU/power/CAN PHY) all the time for every single one-off ECU?

Then TinySparrow is for you! This cute little board combines a [STM32F103TB](https://www.st.com/en/microcontrollers-microprocessors/stm32f103tb.html) MCU,
CAN transceiver, power regulation, and reverse polarity protection all in a single board, so it's ready
to be integrated in all your CAN-enabled device ideas.

Just provide a power source (+5V to +15V DC) and you're good to go. For automotive applications,
the only external component you should bring is load dump protection (often a TVS diode).
