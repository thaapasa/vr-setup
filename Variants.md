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

See https://github.com/capilus/HP-Reverb-G2-index-Controller-HTC-vive-tracker-Working-native-Open-VR
for a setup that uses [OpenVR Input Emulator](https://github.com/matzman666/OpenVR-InputEmulator/releases).
The patched driver file goes to
`C:\Program Files (x86)\Steam\steamapps\common\SteamVR\drivers\00vrinputemulator` (or similar).

You probably need to switch to SteamVR Beta Channel in either case.

## Help with gray screen

- https://www.reddit.com/r/MixedVR/comments/jzk65t/wmr_hmd_steam_vr_controllers_causes_grey_screen/
- https://steamcommunity.com/app/250820/discussions/3/2266942917228868808/
- https://github.com/pushrax/OpenVR-SpaceCalibrator/issues/18
- https://github.com/PumkinSpice/MixedVR/wiki/ReadMe#using-steamvr-chaperone-instead-of-wmr-bounds
