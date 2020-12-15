# My Home Assistant configuration

Currently running a Home Assistant Container install on an ASUS laptop with an i7-2630QM (quad-core 2.0 GHz up to 2.9 GHz) and 8GB of RAM.

The `conf` directory (which is in the same directory as my configuration) contains all of my automations, scripts, etc. `conf_settings` contains things like `recorder`, `history`, `http` and so on. `conf_static` contains configs that I won't need to update often. 

I currently have the following devices connected to Home Assistant:
- Philips Hue
- Ecobee thermostat (local control via Homekit Controller)
- Google Home speakers
- Abode security system (local control via Homekit Controller)
- Zigbee/Z-wave adapter (model HUSBZB-1, currently only using the Z-wave radio)
    - Monopricep power strip with energy monitoring
    - First Alert smoke alarm (ZCOMBO)
- ZZH! Zigbee adapter
    - Ecolink contact sensors
    - Ikea Tradfri outlets
    - Linkind outlets
    - Linkind buttons
    - SmartThings buttons
    - SmartThings water leak sensors
    - Aqara temp/humidity sensors
    - Sengled light strip
    - Leedarson four-button remotes
- APC UPS
- GSM modem for SMS notifications (Huawei E3531)
- Wyze camera (with the custom Dafang firmware)
- Wyze sense contact sensors and motion sensors
- A bunch of Tasmota smart plugs/switches
- IR blasters flashed with Tasmota
- Sonoff RF bridge flashed with Tasmota and Portisch firmware
- Unifi access point
- Vizio TVs
- Roku TV
- A single Tasmota light bulb

Some of my favorite automations include:
- Adjusting my Google Home speakers' volume depending on which app is casting to them (since streaming radio is noticeably quieter than casting music from Google Play Music or Spotify)
- Enabling sleep mode (lights and media players off, security system armed, play white noise) when my fiancee or I press the buttons on our nightstands)
- Turning the lights and media players off and setting the thermostat to away when the security system is armed away
- Resuming the thermostat schedule when the security system is disarmed from away mode at night (and turning on certain lights if it's at night)
- Turning the lights off when the living room TV is turned on at night (and back on when the TV is turned off)
- Turning on the front closet light when the closet door is opened

As you can see, I have split out my configuration pretty substantially (I like keeping it clean). As you can also see, I strongly prefer this style of creating lists:
```yaml
foo:
- bar
- bar
```
rather than this style:
```yaml
foo:
  - bar
  - bar
```
The hyphen counts as an indent, so I find it redundant to use the second method. Others may disagree. Oh well, can't please everyone.
