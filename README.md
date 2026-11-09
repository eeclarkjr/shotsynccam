# ShotSyncCam

ShotSyncCam is a companion iPhone app for Wi-Fi body cameras. It joins the camera’s own access point, shows live view, captures stills, starts and stops recording, pulls clips to the phone, and keeps an on-device library.

This repository hosts the public **support** and **privacy** pages for the app (GitHub Pages). The iOS app source is not included here.

**Supported cameras:** VIEVU LE4 family (Wi-Fi network names typically look like `LE4-XXXXXX`).

ShotSyncCam is a third-party companion app and is not affiliated with or endorsed by VIEVU.

## Features

- **Connect** — Join camera Wi-Fi from the app, reconnect to your usual network when finished, remember previously joined cameras, show a pick list when more than one is saved, and add a camera by Wi-Fi name
- **Status** — Read camera status (including battery and firmware) and sync the camera clock to the phone
- **Camera (live)** — Live view, capture still, start/stop recording, and a rotate control for cameras without an orientation sensor
- **Pull** — Download clips from the camera with progress, speed, ETA, and resumable transfers
- **Library** — Browse pulled stills and videos (day picker, Videos/Stills filters), on-device AVI → MP4 conversion, share clips, and access files in the Files app under On My iPhone → ShotSyncCam
- **Appearance** — Follows the system light and dark appearance

## Requirements

- iPhone
- iOS 15.0 or later
- A supported camera with its Wi-Fi access point turned on

## Getting started

1. Power on the camera and confirm its Wi-Fi network appears (name like `LE4-XXXXXX`).
2. Open ShotSyncCam and allow **Location** and **Local Network** when asked (Location is used only to read the current Wi-Fi name).
3. On the Connect tab, tap **Connect to Camera Wi-Fi**. If several cameras are saved, choose one from the pick list, or tap **Add camera** and enter the Wi-Fi name.
4. Use Status, Camera, Pull, and Library as needed. When finished, tap **Reconnect to Home Wi-Fi**.

Full steps, including how to turn camera Wi-Fi on from a serial console: [Support](support.html).

## Used cameras and Wi-Fi (important)

- **New cameras** usually ship with Wi-Fi On. No special cable is needed.
- **Used or former agency cameras** may have had Wi-Fi turned Off in VIEVU’s desktop software. That saved setting is reapplied every time the camera starts, so no network appears and the iPhone app cannot turn Wi-Fi on by itself.
- Turning it on again requires either the VIEVU USB-to-serial (FTDI) console cable (`custom wifi on` at the `cmd>` prompt — lasts only until the next power-off) or VIEVU’s discontinued desktop software (VIEVU Solution / VERIPATROL; discontinued July 2025).
- Without the cable or that software, you cannot enable Wi-Fi on a camera that was saved as Off.
- If the camera will not stay on without being plugged in, charge the battery fully and try again.
- Before buying a used LE4, ask whether its Wi-Fi network appears when powered on.

Details and serial console steps: [Support — Turn on camera Wi-Fi](support.html#camera-wifi).

## Troubleshooting

- **No camera network / can’t connect** — Make sure camera Wi-Fi is on (see the used-camera note above and the [support guide](support.html#camera-wifi)). Allow Location and Local Network for ShotSyncCam in iOS Settings.
- **Several cameras** — Use the pick list, or **Add camera** with the exact Wi-Fi name.
- **Where are my clips?** — In the app’s Library, and in Files → On My iPhone → ShotSyncCam.
- **Camera time wrong?** — Open Status and use **Sync camera clock to Host**.
- **Will other cameras work?** — Not yet; only the VIEVU LE4 family is supported.

More help: [Support](support.html).

## Privacy

ShotSyncCam does not collect, store, or share personal data. There are no accounts, analytics, advertising, or tracking. Clips stay on your device unless you choose to share them.

Full policy: [Privacy Policy](privacy.html).

## Repository contents

| File | Purpose |
|------|---------|
| `index.html` | Site home with links to privacy and support |
| `support.html` | End-user support (Wi-Fi, connecting, FAQ) |
| `privacy.html` | Privacy policy |
| `README.md` | This file |

## Building the iOS app

The iOS app source is **not** in this repository. This repo only publishes the support site and privacy policy.
