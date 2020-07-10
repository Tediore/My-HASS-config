# My Home Assistant configuration

Currently running a Home Assistant Container install on a mini PC with a dual-core Celeron N3060 (1.6 GHz up to 2.5 GHz) and 4GB of RAM. Runs great and is more than enough for my needs.

The `conf` directory (which is in the same directory as my configuration) contains all of my automations, scripts, etc. `conf_settings` contains things like `recorder`, `history`, `http` and so on. `conf_static` contains configs that I won't need to update often (such as `zha` and `zwave`). 

I currently have the following devices connected to Home Assistant:
- Philips Hue
- Ecobee thermostat (local control via Homekit Controller)
- Google Home speakers
- Abode security system
- Zigbee/Z-wave dongle (model HUSBZB-1)
    - Water leak sensors (SmartThings)
    - Temp/humidity sensors (Aqara)
    - Buttons (SmartThings)
    - Light strip (Sengled)
    - Power strip with energy monitoring (Monoprice)
    - Smoke alarm (First Alert)
- APC UPS
- Xbox One via Xbox REST server
- GSM modem for SMS notifications (Huawei E3531)
- Wyze camera (with the custom Dafang firmware)
- Wyze sense contact sensors and motion sensors
- Unifi access point
- TP-Link smart plugs
- HP Printer (via IPP)
- Vizio TVs
- A few ESPHome smart plugs
- A single LIFX lamp

The only device I have connected to Home Assistant that can't be controlled locally is my Abode security system (though, once the HomeKit firmware is finalized for it, I'll be able to control that locally).

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
