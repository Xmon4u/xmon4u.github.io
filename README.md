# xmon4u.github.io

[![Live Site](https://img.shields.io/badge/Live-xmon4u.github.io-4c8dff.svg)](https://xmon4u.github.io)

Personal site of **XMON4U** — developer and hacker on Kali Linux.

The page is laid out like a Linux `man` page (`XMON4U(1)`) and opens with a small interactive terminal.

## Features

- **Interactive terminal**: type `help`, `whoami`, `ls`, `open <n>`, `stack`, `socials`, `contact`, `music` or `clear`. Up/down arrows for history, Tab to complete.
- **Projects**: my public GitHub repos, grouped by area (security & AI, stream tooling, desktop apps, automation).
- **Music bar**: a tmux-style status bar at the bottom plays the tracks in `music/playlist.json`. Off until you press play; nothing loads before that.
- **Contact form**: sends through Formspree and shows an error if the message doesn't go through.
- **Lightweight**: one HTML file, no frameworks, no icon fonts. About 0.2 MB on first load.
- Responsive down to phone width, keyboard accessible, respects reduced-motion settings.

## Running locally

The music bar fetches `music/playlist.json`, so serve the folder over HTTP instead of opening `index.html` directly:

```bash
git clone https://github.com/Xmon4u/xmon4u.github.io.git
cd xmon4u.github.io
python -m http.server 8080
```

Then open <http://localhost:8080>.

## Editing

- **Projects**: edit the `<section id="projects">` list in `index.html`. The terminal's `ls` command reads the same list, so there is only one place to update.
- **Tracks**: add the mp3 to `music/` and an entry to `music/playlist.json` (`title` and `file`).
