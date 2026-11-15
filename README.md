# Semusika 🎧

**Your sound, your space.** Semusika is a mobile-first music discovery and player web app, designed to grow into an installable Android experience.

## Current status — v0.1
- Responsive web music-player interface.
- Search songs in the Indonesia iTunes Search catalog.
- Play official preview clips where a preview is provided (typically around 30 seconds).
- Favorites and recently played history stored locally in the browser.
- Create personal playlists (playlist metadata is stored locally).
- PWA manifest and service worker shell caching.
- Basic playback controls, seek, volume, shuffle and repeat.

## Run locally
No build step is required. Serve this folder using any static web server, or deploy it to a static hosting provider. Search requires an internet connection.

## Important audio-source limitation
The initial integration uses the public iTunes Search API for discovery and the preview URLs returned by that API. These are preview clips, not full-length on-demand streams. Availability and usage are controlled by the source provider. Semusika does not scrape YouTube, Spotify, or other services, and does not bypass their playback restrictions.

The multi-source architecture is a roadmap, not a claim that all catalogs are already connected. Future providers must explicitly permit the intended playback use and comply with their API terms and licensing.

## Background playback & Android
The current version uses the browser audio element. Playback may continue in a browser tab, but reliable lock-screen controls and background playback across Android devices require additional testing and a native Android media session / foreground playback integration (for example, a Capacitor-based Android shell). This is not yet implemented in v0.1.

## Roadmap
- [x] v0.1 responsive UI, search preview, favorites, local playlist creation, PWA shell
- [ ] v0.2 provider adapters and additional licensed catalogs
- [ ] v0.3 playlist track management, album/artist/genre views and queue
- [ ] v0.4 Android background audio service and lock-screen media controls
- [ ] v0.5 account sync and cloud library
- [ ] v1.0 Android APK release and device testing

## Project structure
```
semusika/
├── assets/
│   ├── cover.svg
│   └── icon.svg
├── app.js
├── index.html
├── manifest.json
├── service-worker.js
├── style.css
└── README.md
```

## License
No license has been added yet. Add a license before accepting external contributions or redistributing the project.
