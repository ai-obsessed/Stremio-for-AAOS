# Stremio for Android Automotive OS (AAOS)

![Stremio on car display - Discover catalog](screenshots/dashboard-discover.png)

![Stremio on car display - Video playback](screenshots/video-player.png)

A modified build of Stremio for mobile v2.5.0 (`com.stremio.one`) adapted for horizontal Android Automotive OS screens. Tested on the 15.4" Polestar 4 display (1920x1200), but works on other landscape AAOS screens.

The stock mobile Stremio APK assumes a vertical phone. On a wide car screen:

- The Home screen jams 14 tiny posters across a single row, leaving the bottom half of the screen empty.
- The Discover catalog forces 7 narrow columns, making poster text unreadable and touch targets too small.
- The Search screen displays inconsistent shelves (7, 11, and 15 items), with posters sliced in half at the right margin.
- Settings are squished into a 210px strip on the far left, leaving over 75% of the screen as dead black space.
- The video player HUD disappears after 3 seconds, drops touch taps, and hides the timeline and bottom controls.
- The player keeps a useless phone screen-rotation button, while the video scaling button opens a broken screen.

This build patches the layout and touch handling so Stremio actually fits a widescreen car display.

## What changed

### Home, Discover, and Search
- Fixed 6-poster shelves across Home, Discover, and Search. Poster size increased from ~94x140px to ~228x342px (nearly 6x the surface area).
- Clean margins with zero clipped or cut-off posters at the right edge.
- Rating badges (IMDb, Rotten Tomatoes) stay neatly inside each card.
- Discover catalog reduced from 7 cramped columns to 6 comfortable 2:3 cinema columns with smooth vertical scrolling.
- Top filter chips moved down with extra padding so the vehicle status bar does not cut them off.

### Navigation rail
- Widened the left sidebar from 80dp to 140dp.
- Enlarged navigation icons from 25dp to 42dp and labels from 12sp to 18sp.
- Touch target height set to 72dp minimum so you can hit Search, Home, Discover, Library, Addons, and Settings from the seat without leaning forward.

### Video player
- Player HUD stays visible while parked. It will not vanish after 3 seconds or force you to tap repeatedly to wake it up.
- Added dedicated -10s and +10s skip buttons with 96dp touch targets.
- Play and pause button enlarged to a 136dp touch target with a 72dp center glyph.
- High-visibility seekbar with a 64dp touch hit area, 8dp visual track, 24dp thumb, and large 24sp timestamps (`44:32` / `01:29:57`).
- Restored the 5 bottom action buttons (Subtitles, Audio Tracks, Playback Speed, Video scaling, Player) at 80dp height, 36dp icons, and 24sp text.
- Fixed the video scaling toggle: properly cycles Fit, Crop, Stretch, and Original instead of opening a broken menu.
- Removed the mobile screen rotation button.
- Fixed touch event handling so taps on controls are never dropped by the system wake filter.

### Stream source selection
- Replaced raw torrent strings with clean stream cards showing resolution (4K, HD), debrid status (Instant Play), and audio formats (Dolby Vision, Atmos, TrueHD).
- Large circular play buttons for easy tapping.
- Quick filter tabs at the top (All, TVFlix) to isolate preferred scrapers.

### Settings and addons
- Settings expanded from the 210px mobile strip to a 1,195px widescreen layout across the display.
- Two-column alignment: setting names on the left, oversized touch buttons and switches on the right.
- Buttons and dropdowns scaled to 56-64dp height with generous 72dp row spacing.

### Install
Download `com.stremio.one-2.5.0.1-AAOS.apk` from [Releases](https://github.com/ai-obsessed/Stremio-for-AAOS/releases).

1. Open the car browser (Vivaldi), download the APK, and tap install.
2. Allow installation from unknown sources if prompted. You can also install it via USB drive.

---
*For parked use only (charging stops, waiting in the car).*  
*Independent community mod. Stremio is a trademark of SmartCode OOD and is not affiliated with this project.*
