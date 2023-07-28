# V0-kirigaml_bed
## RGB lights for kirigaml.

### The klipper-led_effect plugin is required.  
### Installation is as follows: Use an SSH connection to enter the command  
```Bash
cd ~
git clone https://github.com/julianschill/klipper-led_effect.git
cd klipper-led_effect
./install-led_effect.sh
```
### You need to add the configuration of the light effects inside the `printer.cfg` file.
```Bash
[neopixel neopixel]
pin:XXX                            # Motherboard RGB Pin Definition  
chain_count:8                      # Number of lamp beads  
color_order: GRB                   # colour sequence  
initial_RED: 0.2                   # Red. Maximum 1.  
initial_GREEN: 0.2                 # Greener. Maximum 1.  
initial_BLUE: 0.2                  # Blue. Maximum 1.  
  
[led_effect panel_idle]  
autostart: true                    #Automatic operation  
frame_rate: 10                     #Refresh rate  
leds:  
   neopixel:neopixel               #Called RGBs  
layers:  
    comet  1 1 top (.5,0,.5),(.1,.1,0),(0,.5,.5)  
```
Design Idea Sources：    
https://github.com/julianschill/klipper-led_effect/tree/master  
https://github.com/christophmuellerorg/voron_0_kirigami_bed  
https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/VinnyCordeiro/RGB_LED_grid_for_SB  
