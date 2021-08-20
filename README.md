# HP Reverb G2 extended

## Index Controllers

Original instructions: https://github.com/PumkinSpice/MixedVR/wiki/ReadMe?utm_source=pocket_mylist

Note: OpenVR Space Calibrator should only be needed when using the tracking
provided by WMR (i.e., the Reverb G2 HMD). If you use Vive Tracker with the
G2, then it should not be needed.

## MixedVR Manager

See https://github.com/monstermac77/vr#MixedVR-Manager

Install this for some automatic environment management (shutting down WMR / base stations etc. automatically).

Also see https://github.com/Xavr0k/ChaperoneTweak

## HMD tracking with Vive Tracker

See https://github.com/Yersi88/WMR-and-Vive-Tracker for a setup that doesn't rely on
emulator software (OpenVR Input Emulator).

See https://github.com/capilus/HP-Reverb-G2-index-Controller-HTC-vive-tracker-Working-native-Open-VR
for a setup that uses [OpenVR Input Emulator](https://github.com/matzman666/OpenVR-InputEmulator/releases).
The patched driver file goes to
`C:\Program Files (x86)\Steam\steamapps\common\SteamVR\drivers\00vrinputemulator` (or similar).

You probably need to switch to SteamVR Beta Channel in either case.
