# Bosch BMA400 Breakout Board

> [!WARNING]
> The information and material (code, designs, files, ...) are provided "AS IS". We make no representation or warranty of any kind, express or implied, regarding the accuracy, adequacy, validity, reliability, availability, or completeness of any information or material. Use this at your own risk.

> [!WARNING]
> At the time of writing this PCB has not even been produced yet, and as such, it has not even been tested yet! Once it has been properly tested, I will confirm that everything works as expected.

## Introduction

This is a breakout board for the Bosch BMA400 acceleration sensor.

[https://www.bosch-sensortec.com/products/motion-sensors/accelerometers/bma400/](https://www.bosch-sensortec.com/products/motion-sensors/accelerometers/bma400/)

<img src="images/pcb.png" width="600">

## Change Log

* v1.1
  * Modified BMA400 footprint for easier soldering by hand

* v1.0
  * Initial design 

## Design Considerations

* we chose for I2C connectivity, instead of SPI (chip supports both)
* VDD = VDDIO = 3.3V

## Schematics 

<img src="images/schematics.png" width="600">

## How to Obtain the Physical PCB

<img src="images/pcb.png" width="600">

The Gerber file is in this repository (`gerbers/BMA400-breakout.zip`). Simply upload this file a PCB manufacturer of your choice (JLPCB, PCBWay, ...), and you they will make it for you for as low as \$5 for 5 pieces (with the cheapest shipping option, which can take a few weeks).

For JLCPCB, select the order number option where they will replace "JLCJLCJLCJLC" on the board with the actual order number.

> [!WARNING]
> Note that will still have to solder the components onto the PCB yourself!


## How to Edit Design

Everything you need to edit this design in KiCad 8 is included in the repository.

However, this project uses symbols, footprints and 3D models from [Component Search Engine](https://componentsearchengine.com/). Their license allows us to do pretty much whatever we want with them, except redistributing them. For this reason I can't include them in this repository.

If you would like to edit the design yourself, you will need to download the following component libraries from [https://componentsearchengine.com/](https://componentsearchengine.com/) (it's free!):

* [https://componentsearchengine.com/part-view/BMA400/BOSCH](https://componentsearchengine.com/part-view/BMA400/BOSCH)


From the downloaded zip files, move the content of the `KiCad` and `3D` subfolders into the project structure, so that the end-result looks like this:

<img src="images/project_structure.png" width="300">

The KiCad project is configured to look for these files in these locations, using relative paths, so no changes to the project itself are required.	

## Sources

* [https://www.bosch-sensortec.com/products/motion-sensors/accelerometers/bma400/](https://www.bosch-sensortec.com/products/motion-sensors/accelerometers/bma400/)
