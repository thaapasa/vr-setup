# HP Reverb G2 extended

## Index Controllers

Original instructions: https://github.com/PumkinSpice/MixedVR/wiki/ReadMe?utm_source=pocket_mylist

Install [OpenVR Space Calibrator](https://github.com/pushrax/OpenVR-SpaceCalibrator).
Otherwise SteamVR won't show lighthouse-based stuff.
To be checked: is it enough just to set `activateMultipleDrivers: true` to `steamvr.config`?

## MixedVR Manager

See https://github.com/monstermac77/vr#MixedVR-Manager

Install this for some automatic environment management (shutting down WMR / base stations etc. automatically).

Configure `config.bat` before installing. Set lighthouse MAC addresses.
Mine are:
```
D2:F8:C6:7C:A3:A2
DB:A4:D0:19:98:6B
```

Also see https://github.com/Xavr0k/ChaperoneTweak

### Lighthouses

You can also manage lighthouses with Lighthouse keeper: https://github.com/rossbearman/lighthouse-keeper
The MixedVR Manager zip file contains a precompiled version of the lighthouse keeper executable.

## HMD tracking with Vive Tracker

### Option 1

See https://github.com/Yersi88/WMR-and-Vive-Tracker for a setup that doesn't rely on
emulator software (OpenVR Input Emulator).

Configure Vive Tracker to `Steam/config/steamvr.config` (that's my serial there):

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


### Option 2

See https://github.com/capilus/HP-Reverb-G2-index-Controller-HTC-vive-tracker-Working-native-Open-VR
for a setup that uses [OpenVR Input Emulator](https://github.com/matzman666/OpenVR-InputEmulator/releases).
The patched driver file goes to
`C:\Program Files (x86)\Steam\steamapps\common\SteamVR\drivers\00vrinputemulator` (or similar).

You probably need to switch to SteamVR Beta Channel in either case.
