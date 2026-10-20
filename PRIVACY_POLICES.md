# Privacy Policy for MusicNest

**Effective Date:** October 20, 2026

MusicNest is free to use. This page says plainly what the app collects. Playing music, your local files and your playlists stay on your device. A few features use online services, listed below.

---

## 1. What the app collects

- **Account (optional):** if you sign in with Google or email and password (Firebase Authentication), we get your email, display name and profile picture. You can use the player without signing in.
- **Cloud Sync (when signed in):** your account ID, email, name, a MusicNest ID, a short taste summary (play count based) and the last sync time are stored in Firebase Firestore. Sync frequency can be changed or set to Manual in Settings.
- **Usage analytics:** the app uses Firebase Analytics. It records app opens, screens viewed, search terms (first 80 characters), songs you select or play (song ID, title, artist, album), playlist names you create, download events, sign-in events and playback errors. Firebase also adds standard device and app data such as model, OS version and an app instance ID.

  You can turn analytics off at any time in Settings > Account > Usage Analytics. When it is off, no analytics events are collected or sent.
- **Crash reports:** Firebase Crashlytics receives error reports so we can fix crashes.

We do not sell your data and we show no ads in the app.

---

## 2. On-device storage

- **Playlists and history:** playlists, recently played, favorites and queue are stored in a local database on your device.
- **Settings:** appearance, lyrics style and other preferences are stored locally.
- **Local audio:** with media permission, MusicNest scans your device storage only to build an on-device list for playback. File lists are not uploaded.

---

## 3. Other online services

- **Streaming and metadata:** to play and show songs, the app contacts YouTube / YouTube Music, iTunes and lyrics providers with the song title and artist.
- **AI features:** if you use recommendation features, song titles and genre tags can be sent to the AI service you set up (for example a Groq key you enter in Settings).
- **Listen Together:** room codes and the current song ID go through a public relay (ntfy.sh by default) so devices in a room stay in sync.
- **Discord presence (optional):** if you connect Discord, sign-in goes through our auth server and your Discord profile is read to show what you are playing.
- **Playlist import:** the link you paste is read to get the public track list.

Those services have their own privacy policies and see your IP address.

---

## 4. Android permissions

- `READ_MEDIA_AUDIO` / `READ_EXTERNAL_STORAGE`: play audio files on your device.
- `INTERNET` / `ACCESS_NETWORK_STATE`: streaming, lyrics, sign-in and sync.
- `FOREGROUND_SERVICE` and media playback: background playback and notification controls.
- `POST_NOTIFICATIONS`: playback and update notifications.
- `RECORD_AUDIO`: only for features that listen to audio, such as voice search and song recognition.
- `BLUETOOTH_CONNECT` / `BLUETOOTH_SCAN`: pick and show audio output devices.
- `ACCESS_COARSE_LOCATION` / `ACCESS_FINE_LOCATION`: declared for audio device discovery. The app does not send your location in the events listed above. Firebase may work out an approximate region from your IP address.

---

## 5. Your choices

You can use the app without an account. You can turn usage analytics off in Settings > Account. To delete your account and cloud-synced data, use Settings > Account > Delete My Data in the app, or email support@musicnest.me from your account email. Sign out in Settings, or clear app data in Android settings to remove local data.

---

## 6. Updates

We may update this policy as the app changes. The Effective Date above will change when we do.
