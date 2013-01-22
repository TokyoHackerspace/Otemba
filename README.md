# Otemba

> _Otemba_ : Tomboy in Japanese.

Tokyo Hackerspace's very own Arduino clone.

Why another Arduino clone ?

* Really cheap (< JPY1000 all parts and PCB included, we could sell kits for profit, PCBs only for less profit)

* Great for the introduction to arduino/soldering class.

* We would always have an arduino handy at the hackerspace.

* It would fit nicely in the vending machine! We could sell it on the website. There could be a discount for members, or you could get just the PCB when you join so that you readily have a first project to do at the space (get the parts at akizuki and put it together).

* It has the hackerspace logo and stuff!

* It would make a great final end of a crazy THS guided Akihabara tour. Could be a geek tourist kit.

<img src="https://dl.dropbox.com/u/78009186/Photos/otemba.jpg">

## Board Assembly

Checkout the board (5V version) assembly [instructions](https://dl.dropbox.com/u/78009186/Documents/Otemba_1.0_assembly.pdf).

## Bootloader

For some help burning the bootloader, refer to the Arduino [website](http://arduino.cc/en/Hacking/Bootloader?from=Main.Bootloader).

* 5V/16MHz : use the standard Arduino UNO bootloader,

* 3.3V/8MHz : use the 'Arduino Pro or Pro Mini (3.3V, 8MHz) w/ ATmega328',

* 3.3V/8MHz, no crystal : see the minimal circuit description at the end of this [page](http://arduino.cc/en/Tutorial/ArduinoToBreadboard).

## Upload sketches

To lower cost, the Otemba doesn't have an FTDI serial-to-USB chip on-board. So
to upload sketches to the board, an FTDI serial-to-USB dongle is necessary.
These can be bought from Sparkfun or adafruit. For example here is a
[5V](https://www.sparkfun.com/products/9716?) version and a
[3.3V](https://www.sparkfun.com/products/9873) version, depending on what board
setup you use (normally it is 5V). Here is a cheap ass
[way](http://letsmakerobots.com/node/23728) of making such a cable.

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
* 1x 2.1mm barrel jack [akizuki](http://akizukidenshi.com/catalog/g/gC-00077/)

Regulator and capacitors sold together at [akizuki](http://akizukidenshi.com/catalog/g/gI-00451/).

### Battery Booster (optional)

* 1x HT7705A 5V, 200mA booster [akizuki](http://akizukidenshi.com/catalog/g/gI-02800/)
* 1x 47uF electrolytic capacitor (C6) [akizuki](http://akizukidenshi.com/catalog/g/gP-03120/)
* 1x 22uF electrolytic capacitor (C7) [akizuki](http://akizukidenshi.com/catalog/g/gP-03177/)
* 1x 47uH inductor (L1) [akizuki](http://akizukidenshi.com/catalog/g/gP-03965/)
* 1x Shottky diode, 200 mA [akizuki](http://akizukidenshi.com/catalog/g/gI-03013/)
* 1x Optional connector JST XH-2 (2 pins)

### 3.3V/8MHz version

It is possible to make a 3.3V/8MHz version of the Otemba by using an 
[8MHz crystal](http://akizukidenshi.com/catalog/g/gP-00541/) (instead of 16), the
[TA48M033F](http://akizukidenshi.com/catalog/g/gI-00538/) (instead of TA48M05F)
and the [HT7733A](http://akizukidenshi.com/catalog/g/gI-02799/) (instead of
HT7705A).

In that case, it is also possible to completely omit the crystal, C8 and C9 and run the board on the internal oscillator.

## Get Otemba PCB fabricated

The Gerber files necessary to produce Otemba boards can be downloaded here :
[tar](https://dl.dropbox.com/u/78009186/files/Otemba_v1.0_gerber.tar.gz)
[zip](https://dl.dropbox.com/u/78009186/files/Otemba_v1.0_gerber.zip).

PCB can be fabbed anywhere you like, but if you don't know how to start,
checkout the [Seeed Studio](http://www.seeedstudio.com/) [Fusion PCB
Service](http://www.seeedstudio.com/depot/fusion-pcb-service-p-835.html?cPath=185).
It is cheap and quick. The lowest quantity is 10 boards for 10$.
On their website, simply upload the zip file containing the Otemba Gerber
file. The board size is 5x5 cm. All the default options should work just fine.

## License

2012 (c) TokyoHackerSpace, License [CC-BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/).
