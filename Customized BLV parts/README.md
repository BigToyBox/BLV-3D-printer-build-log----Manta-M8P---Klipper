# Customized BLV parts

To better segment the neopixel light rings, I modifoed the lenses and backplates. Choose an insert, drop in the neopixel ring and attcha the back plate to sandwich it all together. There are small alignment marks to help you line up the leds square in the lens. 


## Custom neopixel parts and code


https://user-images.githubusercontent.com/120577343/209478114-9a8a7863-4ae0-4498-9a60-9b79ae05963c.MOV

https://user-images.githubusercontent.com/120577343/209478135-262ede98-7630-4743-8846-90822e58087a.MOV 

https://user-images.githubusercontent.com/120577343/209478141-fe76ba48-79a5-4c61-93c1-53a307766526.MOV

![lens inserts](https://user-images.githubusercontent.com/120577343/209478146-5daae1e4-7c2e-47a9-84cb-3100dfe6351b.png)



1. Install:
cd ~
git clone https://github.com/julianschill/klipper-led_effect.git
cd klipper-led_effect
./install-led_effect.sh

2. Add to printer.cfg
[include led_configuration.cfg]

[neopixel left]
pin: PC6
chain_count: 32
initial_red: 0
initial_green: 0
initial_blue: 0

[neopixel right]
pin: PA9
chain_count: 16
initial_red: 0
initial_green: 0.2
initial_blue: 0.2

3. Create led_configuration.cfg:

[led_effect panel_idle]
autostart:              true
frame_rate:             24
leds:
    neopixel:left (4,5,12,13)
layers:
    breathing  10 0 top (.1,.2,0)

[led_effect power_idle]
autostart:              true
frame_rate:             24
leds:
    neopixel:right (1,3,5,7,9,11,13,15)
layers:
    breathing  10 0 top (0.2,0.05,0.0)



[led_effect progress_idle]
autostart:              true
frame_rate:             24
leds:
    neopixel:left (17,32)
layers:
    breathing  10 0 top (0.01,.01,.03)

[led_effect bed_effects]
leds:
  neopixel:left (1-8)
  neopixel:right (2,4,6,8,10,12,14,16)
autostart:                          true
frame_rate:                         24
heater:                             heater_bed
layers:
    heater  50 0 add    (.1,0,0)

[led_effect extruder]
leds:
    neopixel:left (9-16)
    neopixel:right (2,4,6,8,10,12,14,16)
autostart:                          true
frame_rate:                         24
heater:                             extruder
layers:
    heater 50 0 add    (.1,0,0)

[led_effect progress_bar]
leds:
    neopixel:left (18-32)
autostart:                          true
frame_rate:                         24
layers:
    progress  -1  0 add         ( 0, 0, .1),( 0, 0.1, 0.6) 

[led_effect critical_error]
leds:
    neopixel:right (2,4,6,8,10,12,14,16)
layers:
    strobe         1  1.5   add        (1.0,  1.0, 1.0)
    breathing      2  0     difference (0.95, 0.0, 0.0)
autostart:                             false
frame_rate:                            24
run_on_error:                          true
