# Induction probe installation


## Two for $11.99

![induction probe](https://user-images.githubusercontent.com/120577343/209856536-03181c22-8ea9-4c1c-b97e-79e202d5d74f.jpg)

Installing an induction probe is not complicated compared to the BL Touch. The reason so many people struggle and fail is because they think the probe is supposed to be powered with 5 volts to provide the required 5 volt output. It needs to be powered at the highest DC voltage you have available on your board. It works with 12 volts but 24 volts is best. I simply use a spare fan port and set the pin to the highest available. 


#### Sample code:

[probe]
pin: !PF6 # set for the pin of YOUR board!

x_offset: 35 # this is the offset for my probe mount to a H2 extruder

y_offset: -28 # this is the offset for my probe mount to a H2 extruder

speed: 20

samples: 2

samples_result: median


#### * Go to the klipper endstop test menu and test the logic using a metal object (I use a metal ruler)
#### ** When testing the probe, have a metal ruler handy. Manually run your gantry up far from the bed try a z home and immediately use your metal ruler to test the probe. If it doesn't stop the gantry, you have time to hit the panic button!



                  
                  
   
