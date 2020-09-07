Another variation of the AdaFruit PowerBoost 1000C (https://www.adafruit.com/product/2465) adapted for Raspberry Pi Zero. This is nearly identical to the PowerBoard (https://github.com/jdimpson/PowerBoard), but this time, with a side card that holds an entire 18650 Lithium Ion cell. As with PowerBoard, adds a  schottkey diode and programmable tactile button and LED and patches the Low Battery (LBO) signal to the Pi via a level shifter. 

More significantly, this board lets you choose whether you want to pick-and-place and reflow your own electronic components, or you can just go out and buy a PowerBoost 1000C. You still have to solder on a diode, the battery holder clips, and (if you want them) the signal LED, programmable button, enable switch, and the level shifting mosfet for the LBO signal. But most of the fiddly parts, notably the U1 and U2 controller chips, you can just use from the standard AdaFruit product. Just solder it into place with the male headers they provide, or get some female headers too (that option makes clearance problems).

Other things worthy of note:
- The MicroUSB connector is not the same foot print as AdaFruit uses in their PowerBoost, because I couldn't figure out which one it was. 
- Python software that works with the LBO signal, button, and LED will be linked here when they are published.
- Auxillary header is provided for USB/5VDC electrical input if you don't want to use MicroUSB.
- Auxillary header is provided for boosted 5VDC electrical output if you want to power something else with this board (in addition to, or isntead of, an RPi Zero). NOte this auxillary output is not protected by the schottkey diode. This is analogous to the USB output header that the original PowerBoost 1000C provides, although the sense resistors used to indicate availability of > 500 mA have been removed.

Changes 
- v1.01: Changed MicroUSB connector to one I can find on Digikey; move battery terminals further from RPi header; used thinner/narrower battery holder; add more plus and minus signs (near battery and the USB input header); improve location of component names; added circles around all used pins (squares around GND). 

TODO 
- Since the battery is now onboard, Figure out how to use NTC resistor ("THERM" in the schematic) to monitor battery temperature. This board provides a header to place the NTC, although I haven't experimented with it so have no recommendation for part to use.
