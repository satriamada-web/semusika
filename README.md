# Semusika 🎧

**Your sound, your space.** Semusika is a mobile-first music discovery and player web app with an installable Android build.

## Current features
- Search and stream public, streamable tracks from the Audius catalog (full track playback where the creator has made the track publicly streamable).
- Search the Indonesia iTunes catalog and play official preview clips (typically around 30 seconds).
- Switch between Audius streaming and iTunes previews in the search page.
- Favorites, recently played history, and local playlists.
- Add tracks to a playlist.
- Playback controls, seek, volume, shuffle, repeat, and Media Session action handlers where supported by Android/WebView.
- PWA shell caching and Capacitor Android APK workflow.

## Audio sources and rights
Audius is a community-uploaded catalog. Semusika uses Audius' documented read-only search and stream endpoints; availability, access gates, creator permissions, and Audius API terms control what can be played. A publicly streamable track is not automatically cleared for reuse in videos, redistribution, or commercial licensing. iTunes results are preview clips only.

Semusika does not scrape YouTube or Spotify, extract their audio, or bypass playback restrictions. Future providers must explicitly permit the intended playback use and comply with their API terms and applicable music rights.

## Run locally
No build step is required for the web app. Serve this folder using a static web server or deploy it to static hosting. Searching and streaming require an internet connection.

## Android and background playback
The app uses the HTML audio element and Media Session handlers. Android lock-screen controls and continued playback depend on device/WebView support and still require real-device testing. A dedicated native foreground media service may be needed for reliable background playback across devices.

## Build Android APK
The GitHub Actions workflow Build Semusika Android APK builds a debug APK on pushes to main. Open the workflow run and download the semusika-debug-apk artifact. The artifact is a debug build for testing, not a Play Store release.

## Roadmap
- [x] Audius full-track streaming source integration
- [x] iTunes preview source integration
- [x] Favorites, recent history, and playlist creation
- [x] Add tracks to playlists
- [x] Media Session action handlers
- [ ] Test Audius playback and source switching on multiple Android devices
- [ ] Improve native background playback and lock-screen controls
- [ ] Account sync and cloud library
- [ ] Signed release APK / Play Store preparation

## Project structure
semusika/
├── assets/
├── app.js
├── index.html
├── manifest.json
├── service-worker.js
├── capacitor.config.json
├── package.json
└── README.md

## License
No project license has been added yet. Add a license before accepting external contributions or redistributing the project.
