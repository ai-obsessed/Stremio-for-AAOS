First release of Stremio modified for Android Automotive OS (AAOS). 

The base version used for this mod is official Stremio for mobile v2.5.0 (`com.stremio.one`). The `.1` suffix denotes the first revision adapting the mobile touch UI for wide automotive screens. Designed and tested on the 15.4-inch display of the Polestar 4 (1920x1200), but may work on other vehicles running AAOS.

### Why this mod was created
Stock mobile Stremio on a 15.4-inch automotive display creates a broken layout: over half the screen is wasted black space, the UI is squashed into the top 35%, text and posters are microscopic, and sidebar touch targets are too small to hit from the seat. This release redesigns and scales the entire interface into a proper landscape automotive experience.

### Changes in this build
#### Layout and navigation
- Left sidebar: Widened navigation rail (80dp to 140dp) with larger touch targets and icons for Search, Home, Discover, Library, and Settings.
- Top filter bar: Added top padding and increased container height from 45dp to 60dp so category chips (Trending, By Name, Movies, Series) sit below the 70px vehicle status bar without getting clipped.
- Catalog shelves: Rebalanced poster row density so 6 full posters display neatly across wide displays without clipping a partial 7th poster at the right edge.
- Filter popups: Enlarged bottom sheet modal headers (24sp) and menu rows (21sp font, 64dp row height, 28dp icons).

#### Movie and series details
- Poster and logos: Scaled hero logos (140dp) and section headers (76dp).
- Typography: Enlarged movie title, release year, runtime, genre badges, plot synopsis, and cast credits to comfortable, readable sizes.
- Action buttons: Enlarged main action buttons to 68dp touch targets with 36dp vector glyphs.
- Addon filter chips: Enlarged padding (28x14dp) and chip fonts (21sp).

#### Video player and playback
- Single-tap HUD: Tapping anywhere on the video brings up the playback HUD immediately, with smooth auto-hide after inactivity.
- Skip buttons: Added dedicated +/- 10s skip buttons directly on the player overlay for fast seeking while parked.
- Screen rotation removed: Removed the unapplicable mobile screen rotation button that has no function on a fixed car display.
- Video scaling: Fixed the aspect ratio button that previously opened an empty sidebar; it now cycles through Fit, Crop, Stretch, and Original modes with on-screen toasts.
- Slim seek bar: Replaced the thick dark background block with a slim 12dp track outline around the 8dp progress bar, preserving the wide 64dp touch hit area and 24dp thumb handle for accurate scrubbing.

#### Settings and addons
- Full-width settings: Removed the hardcoded mobile 400dp width clamp, expanding settings up to 1680dp to fill the widescreen display properly.
- Readable settings: Scaled settings row labels and section titles to 20sp, with 52dp button heights and an enlarged video preview player.
- Addon cards: Enlarged addon cards to 300dp height with 68dp icons and 22sp titles, preventing text truncation.
- Version tag: Displayed as 2.5.0.1-AAOS in Settings.

### Assets
- `com.stremio.one-2.5.0.1-AAOS.apk` (ARM64 vehicle build)  
  SHA-256: `de18015bd9a898d8611a16b3c0207dd0b3f959f13e9333d9e83dd378c0c84202`

### Installation
1. Download `com.stremio.one-2.5.0.1-AAOS.apk` directly on the car using the built-in browser, or transfer the file using a USB drive or phone.
2. Open the downloaded APK to install.
3. If prompted, allow installation from unknown sources.

Note: Intended for parked vehicle use only.
