# Open source WIFI module replacement for Gree/Sinclair/Daizuki/TGM AC units
This repository adds support for ESP32-based WiFi modules to interface with Gree/Sinclair AC units.
It's forked from https://github.com/piotrva/esphome_gree_ac, big thanks to @piotrva for his work!
This is just a small adaptation to fix the fan mode and I've implemented a silent mode (no beeping).
It's now compatible with GRJWB04-J / Cs532ae wifi modules

# Current problems (to fix): 
Commands sometimes are rejected and you need to resend. I think this is because currently no control
command (0x3) packets are being sent. Will try to fix that when I have more time.

# HOW TO 
You can flash this to an ESP module. I used an ESP01-M module, like this one:
https://nl.aliexpress.com/item/1005008528226032.html
So that’s both an ESP01 and the ‘adaptor’ board for 3.3V ↔ 5V conversion (since the ESP01 uses 3.3V and the AC uses 5V).
Create a new project in the ESPbuilder from Home assistant and use my YAML.
Then you should be able to compile it. I think you can flash directly from Home Assistant,
but I downloaded the compiled binary and flashed with: https://github.com/esphome/esphome-flasher/releases

See the photos for wiring.

**USE AT YOUR OWN RISK!**
