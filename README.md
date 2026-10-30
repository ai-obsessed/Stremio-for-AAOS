# Stremio for Android Automotive OS (AAOS)

![Stremio on car display - Discover catalog](screenshots/dashboard-discover.png)

![Stremio on car display - Video playback](screenshots/video-player.png)

A modified build of Stremio for mobile v2.5.0 (`com.stremio.one`) adapted for horizontal Android Automotive OS screens. Designed and tested on the 15.4" Polestar 4 display (1920x1200), but may work on other AAOS vehicles.

Stock mobile Stremio is built for phones. On a car screen it squashes everything into the top third, leaves the bottom half as empty black space, and makes buttons and text microscopic. As the photos above show, this build scales the whole interface to fit the display properly.

### Key changes
- Sidebar, posters, text, and settings scaled up to be easy to read and tap from the seat
- Top filter chips moved down so the vehicle status bar doesn't cut them off
- Catalog rows fit 6 full posters across the screen cleanly
- Player HUD opens on first tap, with +/-10s skip buttons added
- Phone screen rotation removed; video scaling button cycles Fit, Crop, Stretch, and Original
- Settings and addon pages expanded to full screen width

### Install
Download `com.stremio.one-2.5.0.1-AAOS.apk` from [Releases](https://github.com/ai-obsessed/stremio-aaos/releases).

1. Download it directly on the car using the built-in browser (or copy it over with a USB drive or phone).
2. Open the file and allow installation from unknown sources when prompted.

---
*For use while parked only (e.g. charging stops).*  
*Independent community mod. Stremio is a trademark of SmartCode OOD and is not affiliated with this project.*
