# Stremio for Android Automotive OS (AAOS)

![Stremio on car display - Discover catalog](screenshots/dashboard-discover.png)

![Stremio on car display - Video playback](screenshots/video-player.png)

This is a modified build of Stremio adjusted for Android Automotive OS (AAOS) landscape screens. It was designed and tested on the 15.4-inch display of the Polestar 4 (1920x1200), but may work on other vehicles running AAOS.

The base version used for this mod is official Stremio for mobile v2.5.0 (`com.stremio.one`). The `.1` in `2.5.0.1-AAOS` marks the first revision adapting the mobile touch interface for wide horizontal car displays.

This repository does not contain Stremio source code or proprietary assets. Ready-to-install signed APKs are published directly on the [Releases](https://github.com/ai-obsessed/stremio-aaos/releases) page.

## Why this mod was created

Running the stock mobile build of Stremio on a 15.4-inch car screen results in a broken, unusable layout:
- Over half the screen is wasted as an empty black void because the app expects a phone aspect ratio.
- The entire interface is crammed into the top 35% of the display.
- Movie titles, synopses, release years, and cast credits are rendered in microscopic fonts that cannot be read from the driver or passenger seat.
- The left navigation bar is razor-thin, with tiny icons that are difficult to tap accurately while sitting in a car.
- Media posters are squashed into a narrow horizontal ribbon with illegible rating tags.
- Top category and filter pills sit right against or under the native car status bar.
- The video player keeps mobile-only buttons like screen rotation that make no sense on a fixed horizontal dashboard, while lacking practical driving-break controls like quick skip buttons.

This build rebalances the layout, scaling every UI component to fit a wide automotive screen.

## What changed

### Layout and navigation
- Left sidebar: Widened navigation rail (80dp to 140dp) with larger touch targets and icons for Search, Home, Discover, Library, and Settings.
- Top filter bar: Added top padding and increased container height from 45dp to 60dp so sorting chips (Trending, By Name, Movies, Series) sit cleanly below the 70px AAOS system status bar without getting clipped.
- Catalog shelves: Rebalanced poster row density so 6 full posters display neatly across the widescreen layout without clipping a partial 7th poster at the right edge.
- Filter popups: Enlarged bottom sheet modal headers (24sp) and menu rows (21sp font, 64dp row height, 28dp icons).

### Movie and series details
- Poster and logos: Scaled hero logos (140dp) and section headers (76dp) to match the wide display.
- Typography: Enlarged movie title, release year, runtime, genre badges, plot synopsis, and cast credits to comfortable, readable sizes from a normal seating distance.
- Action buttons: Enlarged main action buttons to 68dp touch targets with 36dp vector glyphs.
- Addon filter chips: Enlarged padding (28x14dp) and chip fonts (21sp).

### Video player and controls
- Single-tap HUD: Tapping anywhere on the video brings up the playback HUD immediately, with smooth auto-hide after inactivity.
- Skip buttons: Added dedicated +/- 10s skip buttons directly on the player overlay for fast forward and rewind.
- Screen rotation removed: Removed the unapplicable mobile screen rotation button that has no function on a fixed car display.
- Video scaling: Fixed the aspect ratio button that previously opened an empty sidebar; it now cycles through Fit, Crop, Stretch, and Original modes with clear on-screen toasts.
- Slim seek bar: Replaced the thick dark background block with a slim 12dp track outline around the 8dp progress bar, preserving the wide 64dp touch hit area and 24dp thumb handle for accurate scrubbing.

### Settings and addons
- Full-width settings: Removed the hardcoded mobile 400dp width clamp, expanding settings up to 1680dp to fill the widescreen display properly.
- Readable settings: Scaled settings row labels and section titles to 20sp, with 52dp button heights and an enlarged video preview player.
- Addon cards: Enlarged addon cards to 300dp height with 68dp icons and 22sp titles, preventing text truncation.
- Version tag: Settings shows 2.5.0.1-AAOS.

## Downloads

The signed APK is available under [Releases](https://github.com/ai-obsessed/stremio-aaos/releases):

- `com.stremio.one-2.5.0.1-AAOS.apk`: ARM64 build for vehicles.

## Installation

1. Download `com.stremio.one-2.5.0.1-AAOS.apk` directly on the car display using the vehicle's built-in browser (or transfer the file using a USB drive or phone).
2. Open the downloaded APK file.
3. Allow installation from unknown sources if prompted by the system.

## Safety notice

Use video streaming only when the vehicle is parked, such as during charging stops. Follow all local road laws regarding displays in vehicles.

## Disclaimer

This is an independent community project. Stremio is a registered trademark of SmartCode OOD. This project is not affiliated with, sponsored by, or endorsed by SmartCode OOD. All trademarks belong to their respective owners.
