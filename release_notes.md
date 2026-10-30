First release of Stremio modified for Android Automotive OS (AAOS). Designed and tested on the 15.4-inch display of the Polestar 4 (1920x1200), but may work on other vehicles running AAOS.

### Changes in this build
- Navigation sidebar: Widened sidebar navigation with enlarged touch targets for car displays.
- Top filter bar: Added top padding so sorting and category chips (Trending, By Name, Movies, Series) sit below the AAOS status bar without getting clipped.
- Catalog rows: Adjusted layout density to display 6 full movie posters across wide displays without clipping the 7th poster.
- Player controls: Player HUD responds on the first tap. The video aspect ratio button cycles through Fit, Crop, Stretch, and Original modes instead of opening an empty sidebar. The seek slider has a clean, slim outline with a comfortable touch target.
- Touch sizing: Enlarged IMDb ratings, detail buttons, addon cards, and settings rows for easier interaction while parked.
- Version tag: Displayed as 2.5.0.1-AAOS in Settings.

### Assets
- com.stremio.one-2.5.0.1-AAOS.apk (ARM64 vehicle build)
  SHA-256: de18015bd9a898d8611a16b3c0207dd0b3f959f13e9333d9e83dd378c0c84202
- com.stremio.one-2.5.0.1-AAOS-x86_64-emulator.apk (x86_64 emulator companion)
  SHA-256: 25c10df2b3f3728831ac9881b2c3ebe75387c6a7636aa70ffd7e86eb7e0d6fde

### Installation
1. Download `com.stremio.one-2.5.0.1-AAOS.apk` directly on the car using the built-in browser, or transfer the file using a USB drive or phone.
2. Open the downloaded APK to install.
3. If prompted, allow installation from unknown sources.

Note: Intended for parked vehicle use only.
