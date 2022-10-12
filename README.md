# HP Reverb G2 extended

## Requirements

- HP Reverb G2
- 2 base stations
- 2 Valve Index Controllers
- 2 SteamVR USB Dongles, from e.g. [VRDongles](https://vrdongles.com/)
- HTC Vive Tracker
- 5+m USB 2.0 cable + extension for connecting Vive Tracker

## Software

- Mixed Reality Portal
- OpenXR for Windows Mixed Reality
- Steam
- SteamVR
- Windows Mixed Reality for SteamVR
  - I guess this is required for WMR to work with SteamVR
- OVR Advanced Settings
  - I use this to fix floor positioning and restore chaperone settings that Steam seems to lose constantly
- Optionally: fpsVR
- [Lighthouse Keeper](https://github.com/rossbearman/lighthouse-keeper)
  - For turning lighthouses on and off automatically

## Setup

Original instructions from are from [https://github.com/Yersi88/WMR-and-Vive-Tracker](https://github.com/Yersi88/WMR-and-Vive-Tracker).

### Pair controllers

Pair Index Controllers to USB Dongles:

- Connect only one dongle at a time for pairing
- See instructions from [here](https://github.com/PumkinSpice/MixedVR/wiki/ReadMe) 

### Fix Tracker positioning

See "Apply offset to tracker firmware" in [Yersi's instructions](https://github.com/Yersi88/WMR-and-Vive-Tracker).

### Configure SteamVR tracking overrides for Vive Tracker

Edit `Steam/config/steamvr.config` and append the following configurations, replacing tracker serial with your tracker's serial number (that's my serial in the example):

```json
{
  "steamvr" : {
    "activateMultipleDrivers" : true,
  },
  "TrackingOverrides" : {    
    "/devices/htc/vive_trackerLHR-45F6A89D" : "/user/head" 
  }
}
```

## Miscellaneous

### Specs

- [steamvr.vrsettings](https://developer.valvesoftware.com/wiki/SteamVR/steamvr.vrsettings)

### Help with gray screen

- https://www.reddit.com/r/MixedVR/comments/jzk65t/wmr_hmd_steam_vr_controllers_causes_grey_screen/
- https://steamcommunity.com/app/250820/discussions/3/2266942917228868808/
- https://github.com/pushrax/OpenVR-SpaceCalibrator/issues/18
- https://github.com/PumkinSpice/MixedVR/wiki/ReadMe#using-steamvr-chaperone-instead-of-wmr-bounds

### Performance tips

Stop Holographic shell with (in admin console):

```
logman query HolographicShell -ets
logman stop HolographicShell -ets
```
