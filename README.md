<div align="center">

<img src="screenshots/logo.png" alt="MusicNest logo" width="110" />

# MusicNest

**Ad-free music streaming for Android. Synced lyrics and a clean player.**

[![Latest Release](https://img.shields.io/github/v/release/dev-stack12692/MusicNest?style=for-the-badge&color=blue&label=Latest%20Release)](https://github.com/dev-stack12692/MusicNest/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/dev-stack12692/MusicNest/total?style=for-the-badge&color=success&label=Downloads)](https://github.com/dev-stack12692/MusicNest/releases)
[![Platform: Android](https://img.shields.io/badge/Platform-Android%208.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/dev-stack12692/MusicNest/releases/latest)
![License: All rights reserved](https://img.shields.io/badge/License-All%20Rights%20Reserved-lightgrey?style=for-the-badge)

[**Download**](https://github.com/dev-stack12692/MusicNest/releases/latest) · [**Website**](https://musicnest.me) · [**Report a bug**](https://github.com/dev-stack12692/MusicNest/issues) · [**Support**](mailto:support@musicnest.me)

</div>

---

## Overview

MusicNest is a free Android music app I built because I got tired of ads between songs. Search a song, press play, and keep listening. No audio ads, no paywall.

It is made for Indian listeners first, so the home feed leans towards Hindi and regional music.

> [!NOTE]
> MusicNest is free to use, but it is not open source. This repository only hosts the APK releases, the terms and the docs. The source code is not published and all rights are reserved.

Curious why the app exists at all? Read [My Story](MY_STORY.md), or the short [note from me](screenshots/NOTE.md) in the screenshots folder.

---

## Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Features](#features)
- [What's New in v1.3.2](#whats-new-in-v132)
- [Download](#download)
- [How MusicNest Works](#how-musicnest-works)
- [Privacy and Permissions](#privacy-and-permissions)
- [FAQ](#faq)
- [Limitations](#limitations)
- [Docs](#docs)
- [Feedback and Help](#feedback-and-help)
- [Support the Project](#support-the-project)
- [License](#license)

---

## Screenshots

<div align="left">
  <table style="margin: 0 auto; border-collapse: collapse;">
    <tr>
      <td align="center" style="padding: 15px; border: none;">
        <b>Home</b><br><br><img src="screenshots/home.jpg" width="220" alt="Home" style="border-radius: 12px;"/>
      </td>
      <td align="center" style="padding: 15px; border: none;">
        <b>Now Playing</b><br><br><img src="screenshots/player.jpg" width="220" alt="Now Playing" style="border-radius: 12px;"/>
      </td>
      <td align="center" style="padding: 15px; border: none;">
        <b>Search</b><br><br><img src="screenshots/search.jpg" width="220" alt="Search" style="border-radius: 12px;"/>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding: 15px; border: none;">
        <b>Podcasts</b><br><br><img src="screenshots/podcasts.jpg" width="220" alt="Podcasts" style="border-radius: 12px;"/>
      </td>
      <td align="center" style="padding: 15px; border: none;">
        <b>Your Library</b><br><br><img src="screenshots/library.jpg" width="220" alt="Your Library" style="border-radius: 12px;"/>
      </td>
      <td align="center" style="padding: 15px; border: none;">
        <b>Synced Lyrics</b><br><br><img src="screenshots/lyrics.jpg" width="220" alt="Synced Lyrics" style="border-radius: 12px;"/>
      </td>
    </tr>
  </table>
</div>

---

## Features

These are the features of the current public release, v1.3.2.

<details open>
<summary><b>Streaming & Playback</b></summary>
<br>

- **No audio ads.** MusicNest does not play advertisements between songs, and there is no subscription or paywall - every feature in the app is free.
- **Equalizer.** A built-in equalizer with sliders and saved profiles, so you can tune the sound and switch between your profiles from the player.
- **Smart audio focus.** Incoming calls and unplugged headphones pause and resume playback for you, handled on your device.
- **Media controls.** Notification and lock screen controls, so you can skip, pause and scrub without opening the app.
- **Smart queue.** The queue auto-fills when your songs run out, protects against duplicates, and lets you drag tracks into the order you want.

</details>

<details>
<summary><b>Lyrics</b></summary>
<br>

- **Synced lyrics.** Lines highlight as the song plays, with a sync nudge if a track is slightly off.
- **Karaoke-style fill.** On supported tracks the lyrics fill in word by word as they are sung.
- **Several lyric sources.** Lyrics are matched across multiple providers to find the best available version, and the app tells you plainly when a stream has no lyrics.

</details>

<details>
<summary><b>Discovery & Search</b></summary>
<br>

- **Smart home feed.** Jump Back In, mood categories and daily mixes built from what you listen to.
- **Made for India first.** The home feed leans towards Hindi and regional music.
- **Fast search.** Songs, artists and albums in one place, with suggestions and your recent searches.
- **Podcasts.** A dedicated tab next to music.
- **Recommendations that adapt.** Suggestions respond to what you finish, skip and replay - the design notes are in [how it works](Helps/RECOMANDATION.md).

</details>

<details>
<summary><b>Library & Sharing</b></summary>
<br>

- **Library and playlists.** Favourites, playlists and history, stored on your device.
- **Backup and restore.** Export your local data and restore it when you need to.
- **Share songs and playlists.** Send a link to a friend - it opens in MusicNest if they have the app, or on [musicnest.me](https://musicnest.me) if they don't.
- **Listen Together.** Host a room, share the room code, and friends who join hear the same song in sync with you.
- **Referral rewards.** Invite friends from inside the app and earn rewards for it.

</details>

<details>
<summary><b>Accounts (Optional)</b></summary>
<br>

- **Sign in only if you want to.** You can listen without an account. If you sign in with Google or email, the [privacy policy](PRIVACY_POLICES.md) explains exactly what is stored and synced.
- **Your data stays yours.** Playlists, history and settings live on your device. See [Privacy and Permissions](#privacy-and-permissions) below.

</details>

---

## What's New in v1.3.2

Highlights of the current release, from its release notes:

- Accounts with optional Google sign-in
- Backup and restore your local data
- Podcasts, right in the app
- Built-in equalizer
- Karaoke-style lyrics that fill in word by word, with faster lyrics loading
- Smarter audio focus for calls and headphones
- Share songs and playlists, Listen Together rooms, referral rewards
- Redesigned player, home screen and menus
- Smarter recommendations and improved search with suggestions and recent searches

Full notes on the [v1.3.2 release page](https://github.com/dev-stack12692/MusicNest/releases/tag/v1.3.2).

---

## Download

| Platform | Requirement | Get it |
| :--- | :--- | :---: |
| **Android** | Android 8.0 or newer | [**Latest APK**](https://github.com/dev-stack12692/MusicNest/releases/latest) |

Also available at **[musicnest.me](https://musicnest.me)**.

**Installing:** download the APK, open it, and allow "Install unknown apps" for your browser or file manager when Android asks (`Settings > Apps > Special app access > Install unknown apps`).

**Updating:** grab the latest APK from [Releases](https://github.com/dev-stack12692/MusicNest/releases) or [musicnest.me](https://musicnest.me). If Android refuses to install over your existing version, check that release's notes for its install instructions before removing anything - your playlists and history are stored on the device.

---

## How MusicNest Works

MusicNest is a client interface, not a music host.

- **Streaming.** Audio streams in real time from YouTube / YouTube Music endpoints. MusicNest does not host, store or distribute any music files.
- **Metadata.** Song titles, artists and artwork are resolved through services like iTunes.
- **Lyrics.** Fetched from third-party lyric providers and matched to the track you are playing.

Because of this, song names, artwork and audio belong to their respective owners, and MusicNest is not affiliated with YouTube, Google, Spotify or JioSaavn. If you love an artist, the best way to support them is an official platform subscription - see [About](ABOUT.md) and the [Disclaimer](DISCLAIMER.md).

---

## Privacy and Permissions

The short version: playing music, your local files and your playlists stay on your device. The full policy is in [PRIVACY_POLICES.md](PRIVACY_POLICES.md), written in plain language.

- **No ads, no selling data.** The policy states the app shows no ads and never sells your data.
- **Analytics you can turn off.** The policy says MusicNest uses Firebase Analytics (app opens, screens, searches, songs played, playback errors), and explains how to turn it off.
- **Crash reports.** The policy says Firebase Crashlytics sends error reports so crashes can be fixed.
- **Delete your data.** The policy explains how to delete your account and data, in the app or by email.

**Why the app declares each Android permission, as stated in the privacy policy:**

| Permission | Purpose stated in the privacy policy |
| :--- | :--- |
| Media / audio storage | Play audio files stored on your device. File lists are not uploaded. |
| Internet / network state | Streaming, lyrics, sign-in and sync. |
| Foreground service | Background playback and notification controls. |
| Notifications | Playback and update notifications. |
| Microphone | Only for features that listen to audio, like voice search and song recognition. |
| Bluetooth | Pick and show audio output devices. |
| Location (coarse/fine) | Declared for audio device discovery. The app does not send your location. |

---

## FAQ

**Is MusicNest free?**
Yes. Free to download, free to use, no audio ads, no paywall.

**Is it open source?**
No. This repository hosts the APK releases, the terms and the docs. The source code is not published and all rights are reserved.

**Which devices does it support?**
Android 8.0 or newer. There is no iOS or desktop version.

**Do I need an account?**
No. You can listen without signing in - an account is optional.

**Where does the music come from?**
MusicNest hosts nothing. Audio streams from third-party sources (YouTube / YouTube Music), metadata comes from services like iTunes, and lyrics from third-party providers.

**How do I update the app?**
Download the latest APK from [Releases](https://github.com/dev-stack12692/MusicNest/releases) or [musicnest.me](https://musicnest.me). If Android will not install over your current version, read the install note on that release first.

**How do I report a bug?**
[Open an issue](https://github.com/dev-stack12692/MusicNest/issues) with your phone model and app version, or write to [support@musicnest.me](mailto:support@musicnest.me).

**Found a security problem?**
Please do not open a public issue. Email the maintainer or open a Private Security Advisory under the Security tab - see [SECURITY.md](SECURITY.md).

---

## Limitations

Being upfront about what MusicNest is and is not:

- **Third-party dependent.** Streams, metadata and lyrics come from third-party services. Their availability, accuracy and uninterrupted delivery are not guaranteed and can change without notice. If something does not play, please report it.
- **Provided as is.** The app comes with no warranty - please read the [Terms](TERMS.md) before installing.
- **Android only.** There is no iOS, Windows or web player.
- **Not on the Play Store.** MusicNest is distributed as an APK from this repository and [musicnest.me](https://musicnest.me) only.

---

## Docs

| Document | What it covers |
| :--- | :--- |
| [Terms](TERMS.md) | The rules for using the app. Read these before installing. |
| [Privacy Policy](PRIVACY_POLICES.md) | What the app collects, in plain language, and how to opt out. |
| [Disclaimer](DISCLAIMER.md) | Copyright, content hosting and takedown details. |
| [Security](SECURITY.md) | How to report a vulnerability. |
| [Changelog](CHANGELOG.md) | Notable changes by version. |
| [About](ABOUT.md) | Legal disclaimer and attribution. |
| [My Story](MY_STORY.md) | Why and how MusicNest is built by one person. |
| [Listen Together guide](Helps/LISTEN_TOGETHER.md) | Hosting and joining listening rooms. |
| [Recommendation engine](Helps/RECOMANDATION.md) | How suggestions are generated. |

MusicNest does not host or store any music files. Song names, artwork and audio belong to their respective owners. The app is provided as is, with no warranty. Please use it lawfully and read the [Terms](TERMS.md) before installing.

---

## Feedback and Help

Found a bug or want a feature? [Open an issue](https://github.com/dev-stack12692/MusicNest/issues) or write to **support@musicnest.me**. Bug reports with your phone model and app version help the most.

---

## Support the Project

MusicNest stays free. If you like it and want to buy me a chai, you can pay by UPI.

<div align="center">

<a href="upi://pay?pa=Swapnendu26@ybl&pn=Swapnendu%20Mal&cu=INR">
  <img src="https://img.shields.io/badge/PhonePe-Pay%20via%20UPI-5f259f?style=for-the-badge&logo=phonepe&logoColor=white" alt="Pay via UPI" />
</a>

On mobile, tap the badge. Otherwise pay to UPI ID `Swapnendu26@ybl` (Swapnendu Mal).

</div>

---

## License

Free to use. Source code not published. All rights reserved. No redistribution, modification or reverse-engineering.

<div align="center">
<sub>Built by a music lover, for music lovers.</sub>
</div>
