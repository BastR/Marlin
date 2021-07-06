# Marlin 3D Printer Firmware for Rat Rig V-Core pro

It is a Marlin fork adapted to Rat Rig's V-Core Pro.
<img align="right" width=175 src="https://v-core.ratrig.com/assets/logo_rat_small.png" /><img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />
The hardware configuration is as follows:

<br/>-V-Core Pro 1.3 without EVA
<br/>-BMG + Volcano 0.6mm + BLTouch
<br/>-BTT SKR PRO 1.2
<br/>-BTT TFT35 E3 display
<br/>-6x TMC5160 SPI with sensorless homing
<br/>-All fans are 24Vdc except the hotend fan

Additional documentation can be found at the [Marlin Home Page](https://marlinfw.org/).

## Wiring the SKR PRO

I have reallocated some pins, especially the fan pins, as I have already burnt out one card due to over consumption of power by my dual print fans.
You can bridge or create separate supply lines for the different inputs on the card. Make sure you use the correct cable cross-sections and preferably use connectors.

<br/>Click on the picture to see it in full resolution

![SKR PRO](https://user-images.githubusercontent.com/20129420/124657347-b0f75700-dea2-11eb-9581-7f710452e736.png)


## Building Marlin 2.0

To build Marlin 2.0 you'll need VSCodre. Detailed build and install instructions are posted at:

  - [Installing Marlin (VSCode)](http://marlinfw.org/docs/basics/install_platformio_vscode.html).

You can also use Github desktop which allows you to quickly update your Marlin without having to take the configuration files from 0, only the new code will be merged.


## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
