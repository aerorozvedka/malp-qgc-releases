# QGroundControl-MALP

Ground station for MALP drones — a fork of [QGroundControl](https://github.com/mavlink/qgroundcontrol).

## Why a fork

MALP is a system for combat drones developed by the Czech organisation Aerorozvědka, and this fork
adapts QGroundControl for their tactical use. Stock QGroundControl cannot receive WebRTC video,
which keeps the picture together over the lossy links these drones fly on, and it has no aiming
overlay for estimating range from the video. The fork adds exactly that and keeps everything else
as upstream has it, so it follows QGroundControl's development instead of drifting away from it.

![QGroundControl-MALP: tactical OSD and WebRTC link quality over thermal video](images/QGC-MALP.png)

**[Download the latest release](https://github.com/aerorozvedka/malp-qgc-releases/releases/latest)**

## Features

- **WebRTC video (WHEP)** — a drone that announces a WHEP stream over MAVLink configures the video without typing an address
- **Link quality over the video** — resolution, frame rate, bitrate, packet loss, jitter and NACKs, with an amber or red edge when the link degrades
- **Tactical OSD** — mil reticle with the value of one division, speed / AGL / climb tapes, artificial horizon, gimbal pitch and zoom
- **Tactical OSD settings** — colour and opacity on the Video settings page, turned down for night flying
- **Photo and video feedback** — the captured photo flashes over the video, and the camera's recording messages appear in the same corner
- **Tells itself apart** — ARCZ mark in the toolbar and the version in the application name, e.g. `QGroundControl-MALP-v1.2.1`

Everything else is stock QGroundControl.

## Install

| Platform | File | First launch |
|---|---|---|
| macOS 13+ (Apple Silicon + Intel) | `QGroundControl-MALP-<version>-macOS-universal.dmg` | Unsigned: approve it under System Settings → Privacy & Security |
| Linux x86_64 / Steam Deck | `QGroundControl-MALP-<version>-x86_64.AppImage` | `chmod +x` and run; on the Deck from Desktop Mode |

Each release lists SHA-256 checksums in its notes.

## Versions

Releases are tagged with the fork's version (`v1.2.1`), the same one the application name carries.
The release notes also name the upstream QGroundControl revision each build stands on.
