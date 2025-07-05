# Open source WIFI module replacement for Gree/Sinclair/Daizuki/TGM AC units
This repository adds support for ESP-based WiFi modules to interface with Gree/Sinclair AC units.
It's forked from https://github.com/piotrva/esphome_gree_ac, big thanks to @piotrva for his work!

My fork currently differs from the original code in the following ways:

1) I fixed the fan mode, mine works now for Daizuki/TGM AC's.
2) I fixed the dropping of commands
3) I fixed the rejection of commands
4) I implemented a silent mode (no beeping).
   
It's now compatible with GRJWB04-J / Cs532ae wifi modules

# Current state:
No known problems! if you run into an issue though, please let me know.

# HOW TO 
You can flash this to an ESP module. I used an ESP01-M module, like this one:
https://nl.aliexpress.com/item/1005008528226032.html
So that’s both an ESP01 and the ‘adaptor’ board for 3.3V ↔ 5V conversion (since the ESP01 uses 3.3V and the AC uses 5V).


Create a new project in the ESPbuilder from Home assistant and use my YAML.
Then you should be able to compile it. I think you can flash directly from Home Assistant,
but I downloaded the compiled binary and flashed with: https://github.com/esphome/esphome-flasher/releases

See the 2 photos for wiring (for flashing and the wiring for connecting it to your AC).

**USE AT YOUR OWN RISK!**
