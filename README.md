# Stremio for Android Automotive OS (Polestar 4)

This is a modified build of Stremio adjusted for Android Automotive OS (AAOS) landscape screens, tested on the 15.4-inch center screen of the Polestar 4 (1920x1200).

This repository does not contain Stremio source code or proprietary assets. Ready-to-install signed APKs are published directly on the [Releases](https://github.com/ai-obsessed/stremio-aaos-polestar4/releases) page.

## What changed

Stock mobile and TV builds of Stremio do not fit wide automotive screens cleanly. Posters get cut in half at the edges, buttons are hard to tap from the driver seat, and the top status bar cuts off category labels. This build addresses those issues:

- The left navigation sidebar is wider with larger icons for car touch screens.
- Top filter chips have extra padding so labels like Trending, Movies, and Series sit comfortably below the vehicle status bar.
- Catalog shelves show 6 full posters across the screen instead of slicing off a partial 7th poster at the right border.
- The player HUD responds reliably on the first tap.
- The video scaling button cycles through Fit, Crop, Stretch, and Original modes instead of opening an empty sidebar.
- The seek bar uses a slim track outline while keeping a large touch hit area.
- Detail pages, addon cards, IMDb ratings, and settings rows have larger text and touch targets.

## Downloads

Signed APKs are available under [Releases](https://github.com/ai-obsessed/stremio-aaos-polestar4/releases):

- `com.stremio.one-2.5.0.1-AAOS-Polestar4.apk`: ARM64 build for the vehicle.
- `com.stremio.one-2.5.0.1-AAOS-Polestar4-x86_64-emulator.apk`: x86_64 test build for PC Android Automotive emulators.

## Installation

Installing third-party apps on AAOS requires ADB over Wi-Fi or USB.

1. Turn on Developer Options on your car screen (Settings > System > About > tap Build Number 7 times).
2. Enable Wireless Debugging or USB Debugging.
3. Connect your laptop to the car Wi-Fi and connect via ADB:
   ```cmd
   adb connect <car-ip-address>:5555
   ```
4. Install the car APK:
   ```cmd
   adb install -r com.stremio.one-2.5.0.1-AAOS-Polestar4.apk
   ```

## Safety notice

Use video streaming only when the vehicle is parked, such as during charging stops. Follow all local road laws regarding displays in vehicles.

## Disclaimer

This is an independent community project. Stremio is a registered trademark of SmartCode OOD. This project is not affiliated with, sponsored by, or endorsed by SmartCode OOD. All trademarks belong to their respective owners.
