# Stremio for Android Automotive OS (AAOS)

This is a modified build of Stremio adjusted for Android Automotive OS (AAOS) landscape screens. It was designed and tested on the 15.4-inch display of the Polestar 4 (1920x1200), but may work on other vehicles running AAOS.

This repository does not contain Stremio source code or proprietary assets. Ready-to-install signed APKs are published directly on the [Releases](https://github.com/ai-obsessed/stremio-aaos/releases) page.

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

Signed APKs are available under [Releases](https://github.com/ai-obsessed/stremio-aaos/releases):

- `com.stremio.one-2.5.0.1-AAOS.apk`: ARM64 build for vehicles.
- `com.stremio.one-2.5.0.1-AAOS-x86_64-emulator.apk`: x86_64 test build for PC Android Automotive emulators.

## Installation

1. Download `com.stremio.one-2.5.0.1-AAOS.apk` directly on the car display using the vehicle's built-in browser (or transfer the file using a USB drive or phone).
2. Open the downloaded APK file.
3. Allow installation from unknown sources if prompted by the system.

## Safety notice

Use video streaming only when the vehicle is parked, such as during charging stops. Follow all local road laws regarding displays in vehicles.

## Disclaimer

This is an independent community project. Stremio is a registered trademark of SmartCode OOD. This project is not affiliated with, sponsored by, or endorsed by SmartCode OOD. All trademarks belong to their respective owners.
