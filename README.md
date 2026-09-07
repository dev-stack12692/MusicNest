<div align="center">

# 🎵 MusicNest
### Clean, Native, High-Performance Audio Streaming & Lyrics Client

A modern, distraction-free third-party streaming client featuring syllable-synced live lyrics, intelligent discovery, and first-class tablet/landscape optimization.

---

[![Latest Release](https://img.shields.io/github/v/release/dev-stack12692/MusicNest?style=for-the-badge&color=2563EB&label=Release)](https://github.com/dev-stack12692/MusicNest/releases/latest)
[![Total Downloads](https://img.shields.io/github/downloads/dev-stack12692/MusicNest/total?style=for-the-badge&color=10B981&label=Downloads)](https://github.com/dev-stack12692/MusicNest/releases)
[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/dev-stack12692/MusicNest)
[![License](https://img.shields.io/badge/License-MIT-A855F7?style=for-the-badge)](LICENSE)

<br />

<img width="100%" alt="MusicNest Hero Interface" src="https://github.com/user-attachments/assets/127bbab7-fc03-4818-90c6-0ea2a2fe2204" />

</div>

---

## 📱 User Interface

<table>
  <tr>
    <td width="33.33%" align="center"><b>Discovery & Curated Shelves</b></td>
    <td width="33.33%" align="center"><b>Adaptive Landscape Player</b></td>
    <td width="33.33%" align="center"><b>Syllable-Synced Live Lyrics</b></td>
  </tr>
  <tr>
    <td valign="top">
      <img src="https://github.com/user-attachments/assets/0493e949-6898-4e2c-b439-81a2a6713e9a" alt="Curated Music Exploration" width="100%" />
      <p align="left"><sub>Dynamic genre filters, personalized Speed Dial, and dedicated artist tags.</sub></p>
    </td>
    <td valign="top">
      <img src="https://github.com/user-attachments/assets/e93af09c-4574-435e-9725-6141204864cc" alt="Now Playing Controls" width="100%" />
      <p align="left"><sub>Dual-pane layout tailored for tablets, foldables, and landscape usage.</sub></p>
    </td>
    <td valign="top">
      <img src="https://github.com/user-attachments/assets/4ac4429a-6611-4d6b-9c15-1e620c3e47c3" alt="Synchronized Lyrics" width="100%" />
      <p align="left"><sub>Real-time, syllable-by-syllable autoscroll animations with glow highlights.</sub></p>
    </td>
  </tr>
</table>

---

## ⚡ Key Capabilities

* **Curated Content Discovery:** One-tap contextual mood indexing (*Relax*, *Energize*, *Workout*, *Romance*, *Sad*) paired with personalized listening recommendations.
* **Karaoke-Style Live Lyrics:** Syllable- and line-synchronized scrolling backed by public lyric engines. Toggle between cover artwork and animated lyrics with zero audio interruption.
* **Responsive Architecture:** Fully optimized for compact mobile viewports, large-screen tablets, and foldable displays with adaptive split-pane layouts.
* **Queue & Playback Control:** Background audio persistence, seamless loop modes, integrated sleep timer, and rapid queue reordering.
* **Local Privacy First:** No mandatory sign-in or remote telemetry. Playlists, history, and configuration remain safely on your device.

---

## 📥 Getting Started

### Installation
1. Download the latest release package:  
   👉 **[Download MusicNest APK (v1.1.0)](https://github.com/dev-stack12692/MusicNest/releases/latest)**
2. Locate the `.apk` file inside your device's **Downloads** folder.
3. Tap the file to install. When prompted by Android, choose **"Allow from this source"**.
4. Open **MusicNest** and begin listening.

---

## 🏛️ System Architecture

MusicNest operates strictly as an **on-device client aggregator**. No central stream proxies, remote databases, or intermediate caching servers are maintained.

```text
┌─────────────────────────┐
│     MusicNest Client    │
│  (Android / Local Host) │
└────────────┬────────────┘
             │
             ├──► 1. Handshake & Stream Request ──────┐
             │                                        ▼
             │                             ┌────────────────────────┐
             │                             │  Third-Party Endpoints │
             │                             │  (YouTube / YT Music)  │
             │◄─── 2. Direct Audio Stream ─┴────────────────────────┘
             │
             └──► 3. Real-Time Timestamp Queries ─────┐
                                                      ▼
                                           ┌────────────────────────┐
                                           │ Public Lyrics Engines  │
                                           │ (LRCLIB / Public APIs) │
                                           └────────────────────────┘
