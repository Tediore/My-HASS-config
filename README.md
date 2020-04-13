# My Home Assistant configuration

Currently running Home Assistant Core on Docker on a Raspberry Pi 3B+ with an SSD. Once USB boot is supported on the Pi 4 I'll likely be switching to that.

The `conf` directory (which is in the same directory as my configuration) contains all of my automations, scripts, etc. As you can see, I have split out my configuration pretty substantially (I like keeping it clean). As you can also see, I strongly prefer this style of creating lists:
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
The hyphen counts as an indent, so I find it redundant to use the second method. Others may disagree. Oh well, can't please anyone.

I'll add more about my setup later. For now, it's Xbox time.
