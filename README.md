# Open source WIFI module replacement for Gree/Sinclair/Daizuki/TGM AC units
This repository adds support for ESP-based WiFi modules to interface with Gree/Sinclair AC units.
It's forked from https://github.com/piotrva/esphome_gree_ac, big thanks to @piotrva for his work!

My fork currently differs from the original code in the following ways:

1) fix the fan mode
2) Fix dropping of commands
3) Fix rejecting of commands
4) I implemented a silent mode (no beeping).
   
It's now compatible with GRJWB04-J / Cs532ae wifi modules

# Current states:
No known problems! if you run into an issue though, please let me know.

# HOW TO 
You can flash this to an ESP module. I used an ESP01-M module, like this one:
https://nl.aliexpress.com/item/1005008528226032.html
So that’s both an ESP01 and the ‘adaptor’ board for 3.3V ↔ 5V conversion (since the ESP01 uses 3.3V and the AC uses 5V).
Create a new project in the ESPbuilder from Home assistant and use my YAML.
Then you should be able to compile it. I think you can flash directly from Home Assistant,
but I downloaded the compiled binary and flashed with: https://github.com/esphome/esphome-flasher/releases

See the photos for wiring.

**USE AT YOUR OWN RISK!**
