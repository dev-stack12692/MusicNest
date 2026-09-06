# 🎵 MusicNest

<p align="center">
  <img width="1920" height="1200" alt="MusicNest Home" src="https://github.com/user-attachments/assets/127bbab7-fc03-4818-90c6-0ea2a2fe2204" />
</p>

<p align="center">
  <b>A sleek, distraction-free third-party streaming client featuring live synchronized lyrics, rich artist exploration, and tablet/landscape optimization.</b>
</p>

<p align="center">
  <a href="https://github.com/dev-stack12692/MusicNest/releases/latest">
    <img src="https://img.shields.io/github/v/release/dev-stack12692/MusicNest?style=for-the-badge&color=blue&label=Latest%20Release" alt="Latest Release" />
  </a>
  <a href="https://github.com/dev-stack12692/MusicNest/releases">
    <img src="https://img.shields.io/github/downloads/dev-stack12692/MusicNest/total?style=for-the-badge&color=green&label=Downloads" alt="Downloads" />
  </a>
</p>

---

## 📥 Download

Grab the latest compiled APK directly from GitHub Releases:

- 🚀 **[Download MusicNest APK (Latest Version)](https://github.com/dev-stack12692/MusicNest/releases/latest)**

---

## 🏛️ System Architecture

MusicNest operates strictly as a **client-side frontend aggregator**. It does not maintain audio servers, media databases, or custom caching layers for stream content.

```text
┌─────────────────┐         Stream Endpoint Request         ┌────────────────────────┐
│                 ├────────────────────────────────────────►│  Third-Party Services  │
│  MusicNest App  │                                         │   (YouTube / YouTube   │
│ (Client Device) │◄────────────────────────────────────────┤       Music CDN)       │
└────────┬────────┘          Direct Audio Stream Pipe       └────────────────────────┘
         │
         │ Queries Public Lyric APIs
         ▼
┌────────────────────────┐
│  Synced Lyric Server   │
│  (LRCLIB / Public DB)  │
└────────────────────────┘
```

* **Zero Content Storage:** Media files are piped in real time straight from origin CDN servers to the local audio decoder on the user's device.
* **Direct Handshake:** The app does not act as an audio proxy; playback traffic travels directly between the client's IP and upstream host networks.
* **Stateless Client:** User favorites, playlists, and settings reside completely in on-device local storage.

---

## ✨ Features

### 🎧 Curated Music Exploration
* **Moods & Genres:** Instant one-tap mood filtering across tags like *Relax*, *Romance*, *Energize*, *Party*, *Workout*, and *Sad*.
* **Speed Dial:** Fast access to replay your most frequent tracks and recent favorites.
* **Made for You:** Algorithmic recommendations tailored to your most-played artists.
* **Favorite Creators:** Dedicated artist shelf with custom tags (*Acoustic & Indie*, *Symphonic & Cinematic*, *Modern Bollywood*, etc.).

<p align="center">
  <img width="1920" height="1200" alt="Favorite Creators Shelf" src="https://github.com/user-attachments/assets/0493e949-6898-4e2c-b439-81a2a6713e9a" />
</p>

### 📜 Real-Time Synced Lyrics
* Auto-scrolling karaoke-style synchronized lyrics.
* Dynamic line highlighting in sync with current playback time.
* Effortlessly switch between **Album Art** view and **Synced Lyrics** view with a single tap.

<p align="center">
  <img width="1920" height="1200" alt="Synced Lyrics View" src="https://github.com/user-attachments/assets/4ac4429a-6611-4d6b-9c15-1e620c3e47c3" />
</p>

### 🎨 Responsive & Immersive Player
* **Tablet & Landscape Optimized:** Clean split-screen interface with large visual artwork and controls.
* **Player Utilities:** In-app favorites toggle, playlist manager, offline download button, and a persistent mini-player.
* **Quick Controls Bar:** Built-in sleep timer, equalizer shortcuts, and queue access.

<p align="center">
  <img width="1920" height="1200" alt="Now Playing Album Art" src="https://github.com/user-attachments/assets/e93af09c-4574-435e-9725-6141204864cc" />
</p>

---

## ⚖️ Legal Notice & Non-Hosting Disclaimer

MusicNest is developed strictly as a media player client and user interface wrapper.

1. **No Media Hosting or Storing:**  
   MusicNest does **not** host, store, replicate, upload, or archive any audio, video, or image media on its own servers or databases. All audio playback and metadata are fetched directly on demand from public third-party endpoints, primarily YouTube, in real time.
2. **Third-Party Rights & Copyright Ownership:**  
   All songs, album covers, titles, and trademarks are the intellectual property of their respective owners, original artists, record labels, and YouTube. MusicNest claims no affiliation with, endorsement from, or ownership of any streamed materials.
3. **DMCA & Takedown Inquiries:**  
   Because MusicNest does not host or store any media, removing a stream or video from the upstream source (YouTube) will automatically and instantly prevent it from playing inside MusicNest. If you are a copyright owner wishing to remove content, please submit takedown requests directly to the upstream content host (YouTube).
4. **Non-Commercial & Educational Purpose:**  
   This application is distributed free of charge for non-commercial, experimental, and educational purposes.

---

## 📲 Installation Instructions

1. Download the latest `.apk` file from the **[Releases Section](https://github.com/dev-stack12692/MusicNest/releases)**.
2. Locate the file in your device's **Downloads** folder and tap to install.
3. If prompted by Android, enable **"Install from unknown sources"** or **"Allow from this source"** in your system settings.
4. Open **MusicNest** and enjoy streaming!

---

## 🐞 Feedback & Issues

Have an idea for a feature or found a bug? 

Feel free to open an issue in the **[Issues Tab](https://github.com/dev-stack12692/MusicNest/issues)**.
