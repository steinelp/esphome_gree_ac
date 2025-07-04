# Open source WIFI module replacement for Gree/Sinclair/Daizuki/TGM AC units
This repository adds support for ESP32-based WiFi modules to interface with Gree/Sinclair AC units.
It's forked from https://github.com/piotrva/esphome_gree_ac, big thanks to @piotrva for his work!
This is just a small adaptation to fix the fan mode. It's now compatible with GRJWB04-J / Cs532ae wifi modules

**USE AT YOUR OWN RISK!**

Work is still in progress!

Tested with my Daizuki and TSM AC's, mostly works, sometimes need to send parameter change twice - need to investigate.

Communication protocol is based on my own reverse-engineering.

ESPHome interface/binding based on:
* https://github.com/DomiStyle/esphome-panasonic-ac

**NOTES**
* It was reported [#1](https://github.com/piotrva/esphome_gree_ac/issues/1) that with some changes the code works with Lennox li024ci AC

**TODO**
* Support Timers - maybe unnecessray as timers can be managed by Home Assistant
* Support Time sync - maybe unnecessray as timers can be managed by Home Assistant
