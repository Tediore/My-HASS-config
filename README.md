# My Home Assistant configuration

Currently running a Home Assistant Container install on an Optiplex 5040 (Intel i5-6500 with 24GB of RAM).

The `conf` directory (which is in the same directory as my configuration) contains all of my automations, scripts, etc. `conf_settings` contains things like `recorder`, `history`, `http` and so on. `conf_static` contains configs that I won't need to update often. 

I currently have the following devices connected to Home Assistant:
- 60+ Zigbee devices (zigbee2mqtt)
    - Aqara light sensors
    - Aqara temp/humidity sensors
    - Aqara water leak sensors
    - Ecolink contact sensors
    - Iris motion sensors (gen 3)
    - Leedarson four-button remotes
    - Linkind buttons
    - Linkind contact sensors
    - Linkind water leak sensors
    - Philips Hue lights
    - SmartThings buttons
    - SmartThings water leak sensors
    - Sonoff S31 lite outlets
    - THIRDREALITY contact sensor
    - THIRDREALITY motion sensor
    - THIRDREALITY water leak sensors
    - Tradfri remotes
    - Xfinity contact sensors
- Ecobee thermostat (local control via Homekit Controller)
- Google Home speakers
- APC UPSes (connected via apc2mqtt)
- Xiaomi Bluetooth thermometers (flashed with the custom ATC firmware and connected via ESPHome bluetooth proxy)
- Huawei E3531 GSM modem for SMS notifications (connected via sms2mqtt)
- 50+ Tasmota devices
  - IR blasters
  - Lights
  - Plugs
  - Shelly 1 (with a reed sensor) used to smartify my garage door opener
  - Switches and dimmers
- Vizio TVs
- Roku TV

Some of my favorite automations include:
- Opening the garage door if the garage service door is opened within 3 minutes of arming the alarm (because that means we're driving somewhere)
- Adjusting my Google Home speakers' volume depending on which app is casting to them (since streaming radio is noticeably quieter than casting music from Google Play Music or Spotify)
- Enabling sleep mode (lights and media players off, security system armed, play white noise) when my wife or I press the buttons on our nightstands
- Turning the lights and media players off and setting the thermostat to away when the security system is armed away
- Resuming the thermostat schedule when the security system is disarmed from away mode at night (and turning on certain lights if it's at night)
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