Please see the folder named "Config Files".

This folder contains the printer.cfg file, as well as customizations in the "custom_cfg" folder. Assuming you've only changed the WiFi credentials for the Raspberry Pi, you won't need to do anything with these - however, 
if you reflashed the Raspberry Pi, you'll need to add those files to the printer's "config" directory in the "Machine" tab in the printer's Mainsail web interface.

The Stealthburner LEDs have not been configured or integrated into any macros. You can find out how to do that here: https://github.com/VoronDesign/Voron-Stealthburner/blob/main/Firmware/stealthburner_leds.cfg

There is a BigTreeTech HBB in the front-left skirt of the printer. This functions as a physical macro panel. I have some keycaps printed on them for various purposes, but you can/should swap them out. The BTT HBB has 
not been configured or set up to trigger any macros. If you want to use it, you'll need to connect a USB-C to USB-A cable between the Raspberry Pi and the HBB. You can find out how to configure it here: 
https://github.com/bigtreetech/HBB

The Stealthburner uses an LDO Nitehawk-SB toolhead board. It has a Generic 3950 thermistor strapped to the back of the umbilical anchor. This is used as the chamber thermistor. On the printer's Mainsail web interface, 
you will see a heater named "Heater Chamber" - this is configured to turn the fans under the front lip of the bed on, and effectively uses the bed and fans as a heating element for the chamber. When the bed is hot, the 
panels are all affixed, and the door is closed, you can use this to raise the chamber temperature of the printer for more temperature-sensitive engineering filaments. The fans will automatically turn themselves off when 
the specified temperature is hit, and will turn on again if the temperature begins to fall.

In the "custom_cfg" folder, there is a homing override which causes the printer to home Y prior to X. It does this because the X/Y endstop pod has been relocated to the rear of the printer, so it has to home Y before X 
can hit its endstop trigger. If you'd like to instead use sensorless homing, you can find out how to do that here: https://docs.vorondesign.com/tuning/sensorless.html

Please continue to the next text file, "Slicer Configuration".
