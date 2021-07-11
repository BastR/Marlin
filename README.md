# Marlin 3D Printer Firmware for Rat Rig V-Core 1.3 (V-Core 1.1 upgraded with kinematic bed)

It is a Marlin fork for Rat Rig's V-Core 1.3.
<img align="right" width=175 src="https://v-core.ratrig.com/assets/logo_rat_small.png" /><img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />
The hardware configuration is as follows:

<br/>-V-Core Pro 1.3 without EVA
<br/>-BMG + Volcano 0.6mm + BLTouch
<br/>-BTT SKR PRO 1.2
<br/>-BTT TFT35 E3 display
<br/>-6x TMC5160 SPI with sensorless homing
<br/>-All fans are 24Vdc except the hotend fan

Additional documentation can be found at the [Marlin Home Page](https://marlinfw.org/).

## Building the Vcore 1.3

As mentioned above, the Vcore Pro 1.3 is an improvement of the Vcore Pro 1.1 by adding the fantastic kinematic bed. I chose this solution because of lack of time (<strike>laziness</strike>), because I wanted a low cost upgrade and because I was already happy with my current setup EXCEPT for the Z axis.
I didn't want to switch to EVA either, I had already designed my own extruder, and I didn't want to start from 0 for the XY configuration. So I created a hybrid that can be upgraded quickly while taking advantage of the most significant advance, the kinematic bed.

You should follow the manual available at https://ratrig.dozuki.com/Guide/01.+Z+Axis+Assembly/66?lang=en, some small actions will have to be done differently:

<ol>
<li>Disassemble the existing Z Axis</li>
<li>(optional) Disassemble the bed frame to reuse the two 2040 extrusions as electronic rail</li>
<li>(option) Remove the heatpad from the existing bed</li>
<li>Assemble the Vcore 1.3 following the guide but
<ol>
<li>You have to cut two MGN rail @ 600mm for X & Y</li>
<li>Install the Teachingtech Cable Tie Remix behind the printer, not the on provided by default (https://www.thingiverse.com/thing:4871564/files)</li>
<li>Reinstall the heatpad on the new cast tooling plate (degrease thoroughly before installing, pay close attention to the position of the cables to allow for the installation of the rear ball</li>
</ol>
  
 <img width="1183" alt="Capture d’écran 2021-07-10 à 22 42 58" src="https://user-images.githubusercontent.com/20129420/125205011-669a1f80-e280-11eb-9d6e-d902953d1178.png">


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
