# "The WASP" - a BLV CoreXY printer build with MantaM8P and Klipper

#### This is a log of my BLV mgn cube 3d Printer. I built the the FYSETC kit with Bluerolls metal kit recommended by Ben Levi. 


This guide combines the build guides and metal kit animations from Ben Levi, FYSETC factory videos, and David Husolo's guide on [ifixit](https://www.ifixit.com/Device/BLV_MGN_Cube) to provide a build flow that I followed to assemble my BLV printer. It's not the ONLY way to accomplish the build, it's simply a log of how I worked my way thru the build. 

### Modifications include:
- BTT Manta M8P with their CB1 pi clone
- Klipper firmware
- My own neopixel code controlled directly by the MantaM8P (no daughter board required)
- Microsoft camera 
- Noctua quiet power supply fan per David's guide on ifixit
- Magnetic print bed with spring steel PEI build plate

<img src="https://user-images.githubusercontent.com/120577343/209441926-59236815-ea76-452b-a6a8-aa57b83c054e.JPG" width="900">

<img src="https://user-images.githubusercontent.com/120577343/209441932-90802643-60bf-41d2-a4df-9d9dc0c372d4.JPG" width="300"><img src="https://user-images.githubusercontent.com/120577343/209441933-1b79081c-f190-4107-896e-d7802f7bdb4f.JPG" width="300"><img src="https://user-images.githubusercontent.com/120577343/209441936-9d2571a3-a9d0-4283-993a-68af19670be5.JPG" width="300">

## My build includes the following mods:

3. Neopixels controlled by the Manta board

## STL files
1. Bigtreetech H2 extruder/hermit crab mount adapted to the metal kit 
2. Adapter mount plate from the Duet mounting holes to the Manta M8P board
3. TPU mounting feet
4. Redesigned LED light strip diffusers
5. Redesigned LED neopixel diffusers

## Manta M8P-CB1 firmware
** Firmware


## Configuration Checks

From the Voron website:
![Stepper motor direction setup (voron site)](https://user-images.githubusercontent.com/120577343/209176872-27d13291-3cc7-49af-ba4d-3588370ecf00.png)

## Step 1 - Endstop tests
* Test each endstop by using the "Endstop" tab within the "Machine" page
* Adjust logic as needed by doing research online and/or with your board
    For the Manta M8P ..............TBD

## Step 2 - Motor tests
* Be sure to be ready to manually trip the endstop(s) with your finger if the motor(s) are moving in the wrong direction
