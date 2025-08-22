# My Home Assistant configuration

Currently running a Home Assistant Container install on an OptiPlex 3050 Micro.

The `conf` directory (which is in the same directory as my configuration) contains all of my automations, scripts, etc. `conf_settings` contains things like `recorder`, `history`, `http` and so on. `conf_packages` contains, well, packages.

I currently have the following devices connected to Home Assistant:
- Various Zigbee devices (zigbee2mqtt)
- Ecobee thermostat (local control via Homekit Controller)
- Google Home speakers
- APC UPSes
- Various Tasmota devices
- Google TV
- Roku TV
- Cameras (Frigate)

Some of my favorite automations include:
- The classic: turning lights on in the evening (I swear I don't know how I ever functioned before without this)
- Adjusting my Google Home speakers' volume depending on which app is casting to them (since streaming radio is noticeably quieter than casting music from YouTube Music or Spotify)
- Enabling sleep mode (lights and media players off, security system armed, play white noise) when my wife or I press the buttons on our nightstands
- Turning the lights and media players off and setting the thermostat to away when the security system is armed away
- Resuming the thermostat schedule when the security system is disarmed from away mode (and turning on certain lights if it's at night)
- Turning the lights off when the living room TV is turned on at night (and back on when the TV is turned off)

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