<p align="center">
  <img src="https://cutnotes.app/icon-512.png" alt="CutNotes" width="128" height="128">
</p>

<h1 align="center">CutNotes</h1>

<p align="center">
  <strong>Professional notes for DaVinci Resolve editors.</strong><br>
  Click any timecode in your notes — Resolve's playhead jumps to that frame.<br>
  No copy-paste. No app switching.
</p>

<p align="center">
  <a href="https://github.com/ElOlamirewaju/cutnotes-releases/releases/tag/v1.0.2"><img src="https://img.shields.io/badge/Download-v1.0.2-E8451A?style=for-the-badge&logo=apple&logoColor=white" alt="Download"></a>
  <a href="https://cutnotes.app/"><img src="https://img.shields.io/badge/Website-cutnotes-07090C?style=for-the-badge&logo=safari&logoColor=white" alt="Website"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-macOS%2012%2B-07090C?style=flat-square&labelColor=07090C&color=E8451A" alt="macOS">
  <img src="https://img.shields.io/badge/status-public%20beta-07090C?style=flat-square&labelColor=07090C&color=12C4A0" alt="Beta">
  <img src="https://img.shields.io/badge/version-1.0-07090C?style=flat-square&labelColor=07090C&color=E8451A" alt="Version">
  <img src="https://img.shields.io/badge/license-BSL--1.1-07090C?style=flat-square&labelColor=07090C&color=E8451A" alt="License">
</p>

<br>

<p align="center">
  <img src="https://cutnotes.app/screenshots/01_main_window_hero_shot.png" alt="CutNotes main window" width="900">
</p>

---

## Why CutNotes

You're cutting in DaVinci Resolve. Your notes live in a different app — Notes, Notion, a Google Doc. Every reference to a timecode means: copy from notes → switch to Resolve → paste into the playhead → switch back. Repeat 80 times a day.

CutNotes makes that loop disappear. Your notes app **talks to Resolve directly**. Click a timecode → playhead jumps. Import markers from your timeline → they show up as clickable, color-coded entries in your notes. Export the whole thing as PDF for your director.

> **This is a public beta.** The app works, but it's not yet code-signed by Apple, so install requires two terminal commands (see [Installation](#installation)). Bug reports and feature requests are very welcome — that's the point of the beta.

---

## Features

<table>
<tr>
<td width="50%" valign="top">

### Click-to-Seek Timecodes
Every timecode in your notes is a live link to your Resolve timeline. Click `01:02:33:18` → the playhead is there. No copy-paste, ever.

### Marker Import
Pull markers from your active timeline with full metadata — name, notes, color, frame-accurate timecode. Duplicate detection prevents re-importing the same marker.

### Rich-Text Editor
Bold, italic, underline. The keyboard shortcuts you already know. Auto-save every 2 seconds.

</td>
<td width="50%" valign="top">

### Instant Search
Find any note across all projects and timelines. Real-time highlighting. Filter thousands of notes in milliseconds.

### PDF & TXT Export
Share formatted notes with your director, colorist, or client. Timecodes and formatting preserved.

### Project Organization
Projects → Timelines → Notes. Switch between edits instantly. Everything stored locally in SQLite — your notes never leave your machine.

</td>
</tr>
</table>

---

## Screenshots

<table>
<tr>
<td width="50%" align="center">
<img src="https://cutnotes.app/screenshots/02_marker_import_dialog.png" alt="Marker Import" width="420"><br>
<sub><strong>Marker Import</strong> — Pull from Resolve with color and notes intact</sub>
</td>
<td width="50%" align="center">
<img src="https://cutnotes.app/screenshots/03_export_dialog_pdf.png" alt="PDF Export" width="420"><br>
<sub><strong>Export</strong> — PDF and TXT with formatting preserved</sub>
</td>
</tr>
<tr>
<td width="50%" align="center">
<img src="https://cutnotes.app/screenshots/04_search_highlighting.png" alt="Search" width="420"><br>
<sub><strong>Search</strong> — Real-time highlighting across all notes</sub>
</td>
<td width="50%" align="center">
<img src="https://cutnotes.app/screenshots/05_resolve_connection_indicator.png" alt="Live Connection" width="420"><br>
<sub><strong>Live Connection</strong> — Green dot = connected to Resolve</sub>
</td>
</tr>
</table>

---

## Installation

### 1. Download

Grab **`CutNotes-1.0.2.dmg`** from the [latest release](https://github.com/ElOlamirewaju/cutnotes-releases/releases/tag/v1.0.2).

### 2. Install

Open the `.dmg` and drag **CutNotes.app** into your **Applications** folder.

### 3. Launch

Double-click CutNotes — done.

This build is **Apple-signed and notarized** (Developer ID: Olanrewaju Akinola, Q94Y8B437Y). No terminal commands, no Gatekeeper warnings, no quarantine workaround.

### Verify the download (optional)

```bash
shasum -a 256 -c CutNotes-1.0.1.dmg.sha256
```

---

## Requirements

| Requirement | Details |
|-------------|---------|
| **macOS** | 12.0 Monterey or later (Apple Silicon native) |
| **DaVinci Resolve** | 18.x or 20.x — *optional, CutNotes works standalone* |
| **Python** | 3.14+ — required only for the Resolve integration |

Install Python via Homebrew:

```bash
brew install python@3.14
```

---

## Quick Start

| Step | Action |
|------|--------|
| **1** | Launch CutNotes from Applications |
| **2** | Click the project dropdown → **Create New Project** |
| **3** | Click the timeline dropdown → **Create New Timeline** |
| **4** | Start writing notes |
| **5** | Click **Insert Timecode** to grab Resolve's current playhead position |
| **6** | Click any **highlighted timecode** to seek Resolve to that frame |
| **7** | Click **Import Markers** to pull markers from the active timeline |
| **8** | **Export to PDF** or **TXT** to share with your team |

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `⌘B` | Bold |
| `⌘I` | Italic |
| `⌘U` | Underline |
| `⌘F` | Search notes |
| `⌘Z` / `⇧⌘Z` | Undo / Redo |

---

## Troubleshooting

<details>
<summary><strong>App won't open / crashes on first launch</strong></summary>

The current build is Apple-signed and notarized, so Gatekeeper should accept it without prompts. If you do hit an issue:

1. Re-download from the [release page](https://github.com/ElOlamirewaju/cutnotes-releases/releases/tag/v1.0.2) — partial downloads can corrupt the stapled ticket
2. Verify the SHA-256 matches: `shasum -a 256 -c CutNotes-1.0.1.dmg.sha256`
3. Check Console.app (filter: `CutNotes`) for the actual crash reason
4. [Open an issue](https://github.com/ElOlamirewaju/cutnotes-releases/issues) with the Console output and your macOS version
</details>

<details>
<summary><strong>Resolve connection indicator stays red</strong></summary>

1. Verify Python 3.14 is installed: `python3.14 --version`
2. Launch DaVinci Resolve **before** CutNotes
3. Open a project and timeline in Resolve
4. Wait 5–10 seconds for auto-detection
5. Restart both apps if needed
</details>

<details>
<summary><strong>Imported markers land at the wrong timecode</strong></summary>

CutNotes accounts for timeline start offset (e.g. broadcast `01:00:00:00` start). If timecodes still look off:

1. Check **Timeline → Timeline Settings → Start Timecode** in Resolve
2. Verify timeline FPS matches project FPS
3. Try resetting timeline start to `00:00:00:00` as a sanity check
</details>

<details>
<summary><strong>PDF export comes out blank</strong></summary>

Make sure notes are written in the editor for the **selected timeline** before exporting. Export captures current editor content for the active timeline.
</details>

---

## Roadmap

**v1.0 — Foundation** *(shipped)*
- ✅ Rich-text notes editor with auto-save
- ✅ Live DaVinci Resolve integration (click-to-seek)
- ✅ Marker import with duplicate detection
- ✅ PDF & TXT export
- ✅ Project / Timeline organization
- ✅ Instant search

**v1.0.1 — Auto-update** *(shipped)*
- ✅ Sparkle-based auto-update (EdDSA-signed, atomic)
- ✅ "Check for Updates…" menu item
- ✅ Daily background check

**v1.0.2** *(current beta)*
- Auto-update validation build — no functional changes from v1.0.1.

**v2.0 — Enhanced Productivity** *(Q3 2026)*
- Categories with color coding (VFX, Audio, Color, Edit, Review, Note)
- List View mode for batch operations
- Batch marker creation, deletion, categorization, export
- Windows support (Qt cross-platform)

**v3.0 — Cloud & Collaboration** *(Q2 2027)*
- Cloud sync across devices
- Team projects with shared notes and permissions
- Comments, @mentions, version history
- AI-powered note summarization and auto-categorization

**v4.0+ — Future**
- Premiere Pro / Final Cut Pro / Avid Media Composer integration
- iOS / Android companion app for set notes
- Advanced analytics, Frame.io and Slack integrations

---

## Feedback & Bug Reports

Found a bug? Got a feature idea? **That's exactly what beta is for** — please tell us.

- **Open an issue:** [github.com/ElOlamirewaju/cutnotes-releases/issues](https://github.com/ElOlamirewaju/cutnotes-releases/issues)
- **Include:** macOS version, Resolve version, Python version (`python3.14 --version`), steps to reproduce, screenshots if visual

---

## License

CutNotes is source-available under the **Business Source License 1.1 (BSL-1.1)**.

- ✅ You **can** use it personally, learn from the code, and modify it for non-production use
- ❌ You **cannot** redistribute, resell, or use it commercially without a license
- 📅 On **March 2030**, the license converts to Apache 2.0

---

<p align="center">
  <a href="https://cutnotes.app/">Website</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/ElOlamirewaju/cutnotes-releases/releases/tag/v1.0.2">Download</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/ElOlamirewaju/cutnotes-releases/issues">Report a bug</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/ElOlamirewaju/cutnotes-releases/issues/new?labels=enhancement">Request a feature</a>
</p>

<p align="center">
  <sub>Made for video editors who deserve better tools.</sub>
</p>
