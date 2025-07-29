# Apple1-Analyzer - Single-Stepper-Display-card

**Copyright (c) 2025 Vossi - v 1.1**
**www.mos6509.com**

## License
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0
International License. See [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/)

**in action:**

![cardinslot](https://github.com/vossi1/Apple1-Analyzer/blob/master/photos/analyzer_02_s.jpg) ![screen](https://github.com/vossi1/Apple1-Analyzer/blob/master/photos/analyzer_03_s.jpg)

**description:**

    Apple1 card with these features:

    - address and databus hex display
    - single stepper circuit
    - programmable stop address
    - with cmos 6502 it shows also write cycles
    - OpC LED shows start of new instruction
    - the LED in the step-key shows CPU is stopped and ready for stepping
    - compatible with Wendell Sander's Expansion board (unbufferd mode!)
      * with the expansion, the address lines are also buffered, which is recommended!

![card](https://github.com/vossi1/Apple1-Analyzer/blob/master/photos/analyzer_01.jpg)

**[Schematic](https://github.com/vossi1/Apple1-Analyzer/blob/master/schematic_v11.png)**

**[Parts](https://github.com/vossi1/Apple1-Analyzer/blob/master/parts_v11.txt)**

**function:**

    CFFE: 80 02         programs the stop address to 0280 (lo, hi)
    Enable-switch       activates the stepper
    Stop-key            stops manually
    Start-key           continues
    Step-key            steps cylce by cycle

**comments:**

    GERBER v1.1 have only a minimal change at IRQ+NMI-LED anode, but are still untested!
    GERBER v1.0 are tested and it's only a small cut and connection needed, to connect 
    IRQ+NMI-LED anodes to +5V cut the connection to GND. (File photos/patch_v10.jpg)

    The 7407 is optional for an open collector Ready output. It is only needed if another
    source drives the ready line. The jumper selects if 7407 is present or not.
    
    A 7474 or maybe a 74LS74 should also works, but the FlipFlop drives many TTL inputs.
    
    74HCT374 were used so as not to overload the bus!

    You can use a cheap toggle switch or an ITT shadow on/off switch for Enable.
    
    The LED in the step-key is optional.
    
    You can use TIL311 or DIS1417 hex displays.

**version changes:**

    - v1.1  fixed anodes of IRQ+NMI-LED to +5V.
