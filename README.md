# Otemba

> _Otemba_ : Tomboy in Japanese.


Tokyo Hackerspace's very own Arduino clone.

Main purposes and characteristics:

* Really cheap (< JPY1000 all parts and PCB included, we could sell kits for profit, PCBs only for less profit)

* Great as introduction to soldering

* Great for the introduction to arduino class

* We would always have an arduino handy at the hackerspace

* It would fit nicely in the vending machine! We could sell it on the website. There could be a discount for members, or you could get just the PCB when you join so that you readily have a first project to do at the space (get the parts at akizuki and put it together).

* It would have the hackerspace logo and stuff, it could have a funky shape (a sushi ?).

* It would make a great final end of a crazy THS guided Akihabara tour. Could be a geek tourist kit. (Totti)

[Otemba schematics](https://github.com/TokyoHackerspace/Otemba/raw/master/Otemba_sch.png)

[Otemba board layout](https://github.com/TokyoHackerspace/Otemba/raw/master/Otemba_brd.png)

## Bill Of Materials

* 1x 10K resistor (R1) [akizuki](http://akizukidenshi.com/catalog/g/gR-25103/)
* 1x 1K resistor (R2) [akizuki](http://akizukidenshi.com/catalog/g/gR-25102/)
* 3x 0.1uF capacitors (C1, C2, C3) 2.54mm pitch [akizuki](http://akizukidenshi.com/catalog/g/gP-00090/)
* 2x 22pF capacitors (C8, C9) [akizuki](http://akizukidenshi.com/catalog/g/gP-04060/)
* 1x atmega328p [akizuki](http://akizukidenshi.com/catalog/g/gI-03142/)
* 1x Tactile Switch 2.54mm pitch [akizuki](http://akizukidenshi.com/catalog/g/gP-03652/)
* 1x 16MHz crystal [akizuki](http://akizukidenshi.com/catalog/g/gP-00545/)
* 1x 3mm LED [akizuki](http://akizukidenshi.com/catalog/g/gI-04113/)
* 1x6 and 1x20 pin headers (90 degrees) [akizuki](http://akizukidenshi.com/catalog/g/gC-01627/)
* 2x3 pin header (straight) [akizuki](http://akizukidenshi.com/catalog/g/gC-00082/)


### Regulator (optional)

* 1x TA48M05F 5V, 500mA regulator
* 1x 47uF electrolytic capacitor (C4) 
* 1x 0.1uF capacitor (C5)

Sold together at [akizuki](http://akizukidenshi.com/catalog/g/gI-00451/).

### Battery Booster (optional)

* 1x HT7705A 5V, 200mA booster [akizuki](http://akizukidenshi.com/catalog/g/gI-02800/)
* 1x 47uF electrolytic capacitor (C6) [akizuki](http://akizukidenshi.com/catalog/g/gP-03120/)
* 1x 22uF electrolytic capacitor (C7) [akizuki](http://akizukidenshi.com/catalog/g/gP-03177/)
* 1x 47uH inductor (L1) [akizuki](http://akizukidenshi.com/catalog/g/gP-03965/)

### 3.3V/8MHz version

It is possible to make a 3.3V/8MHz version of the Otemba by using an 
[8MHz crystal](http://akizukidenshi.com/catalog/g/gP-00541/) (instead of 16), the
[TA48M033F](http://akizukidenshi.com/catalog/g/gI-00538/) (instead of TA48M05F)
and the [HT7733A](http://akizukidenshi.com/catalog/g/gI-02799/) (instead of
HT7705A).

In that case, it is also possible to completely omit the crystal, C8 and C9 and run the board on the internal oscillator.

## Bootloader

* 5V/16MHz : use the standard Arduino UNO bootloader,

* 3.3V/8MHz : use the 'Arduino Pro or Pro Mini (3.3V, 8MHz) w/ ATmega328',

* 3.3V/8MHz, no crystal : see the minimal circuit description at the end of this [page](http://arduino.cc/en/Tutorial/ArduinoToBreadboard).
