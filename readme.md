# PanguPlay IPTV (Windows)

A modern Windows IPTV player built with **Electron + Shaka Player** that
supports:

-   MPEG-DASH (`.mpd`)
-   HLS (`.m3u8`)
-   TS streams
-   **ClearKey DRM (KID:KEY)**
-   Custom headers (User-Agent, Cookie)
-   Full M3U playlists
-   Channel groups & logos
-   Search & language/group filter
-   Video quality & audio track selection
-   View modes: Fit / Fill / Stretch / Zoom
-   Persistent settings (saved locally)
-   Windows EXE build (Installer + Portable)

This project exists because most native Windows players do **not**
support ClearKey.\
It uses Chromium's EME through Electron, so anything that plays in a
modern browser will play here.

------------------------------------------------------------------------

## ✨ Features

-   Load **remote M3U URL** or **local M3U file**
-   Parses:
    -   `#EXTINF`
    -   `group-title`
    -   `tvg-logo`
    -   `#KODIPROP:inputstream.adaptive.license_key`
-   Automatic ClearKey playback for DASH streams
-   Channel list with logos
-   Instant search
-   Group / language filter
-   Quality selector (Auto / 240p / 360p / 720p / 1080p etc.)
-   Audio track selector
-   Video view modes
-   Preferences saved with `localStorage`
-   Real Windows app (no browser required)

------------------------------------------------------------------------

## 🧰 Requirements

-   Windows 10 / 11
-   Node.js (LTS): https://nodejs.org/

------------------------------------------------------------------------

## 🚀 Run in Development

``` bash
npm install
npm start
```

This opens the app in a desktop window.

------------------------------------------------------------------------

## 🏗 Build Windows EXE

``` bash
npm run build
```

Output will be created in:

``` text
dist/
 ├─ PanguPlay IPTV Setup.exe   (Installer)
 └─ PanguPlay IPTV.exe         (Portable)
```

No Node.js is required on target machines.

------------------------------------------------------------------------

## 📺 Usage

1.  Launch the app\
2.  Load a playlist:
    -   Paste M3U URL and click **Load**, or
    -   Choose a local `.m3u` file\
3.  Browse channels\
4.  Click a channel to play\
5.  Use:
    -   Search box to filter
    -   Group selector for language/categories
    -   Quality & audio selectors
    -   View mode for screen fitting

ClearKey streams play automatically when `license_key=KID:KEY` is
present.

------------------------------------------------------------------------

## ⚠️ Disclaimer

This project is for **educational and personal use** only.\
You are responsible for the content you load and must respect all
applicable laws and service terms.

------------------------------------------------------------------------

## 🧑‍💻 Author

**PanguPlay**

Built to solve real-world IPTV & DRM playback limitations on Windows.
