# 📝 Changelog

All notable changes to **MusicNest** will be documented in this file.  
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [1.1.0] - 2026-09-07

### Added
- **AI Recommendation Engine:** Generates track recommendations based on ongoing listening context.
- **Smart Queue:** Auto-filling queue when tracks run out, with duplicate protection and drag-to-reorder.
- **Dynamic Synced Lyrics:** Real-time syllable-by-syllable text highlighting and wipe effects.
- **Lyrics Customization:** Options to select lyric animations, glow intensity, and text size.

### Improved
- Memory usage during long playback sessions reduced by ~20%.
- Screen real-estate utilization on compact mobile displays.
- Responsive layout for tablet and landscape orientations.

### Fixed
- Audio focus loss when navigating between background and foreground playback.
- Intermittent lyric desynchronization on variable-bitrate streams.

---

## [1.0.0] - Initial Release

### Added
- Core audio player using Media3 / ExoPlayer.
- Stream playback from public endpoints.
- Basic queue management.
- Simple line-by-line synced lyric parsing.
- Material 3 dark/light interface.
