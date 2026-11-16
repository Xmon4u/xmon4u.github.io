# xmon4u.github.io

[![Live Site](https://img.shields.io/badge/Live-xmon4u.github.io-4c8dff.svg)](https://xmon4u.github.io)

Personal site of **XMON4U**: developer and hacker on Kali Linux.

It's a hacker-themed portfolio. An animated ASCII background reacts to the cursor and the music, and the page builds itself piece by piece the first time you visit. A working terminal and a few secrets are hidden around it.

## Features

- **Build intro**: on the first visit (then once every 24 hours) the site assembles itself section by section, with a build log and its own soundtrack. Run it again any time with Ctrl+K → *New build*, or `make` in the terminal.
- **Interactive terminal**: type `help` to see the commands. Up and down arrows go through history, Tab completes.
- **Command palette**: Ctrl+K for themes, music, the build and the fun stuff.
- **Themes**: Kali, Parrot, BlackArch and Matrix colour schemes.
- **Music**: a status bar player with a volume slider. It stays off until you press play, and the background moves with the beat.
- **Projects from GitHub**: the cards re-sort from the GitHub API, so the repo pushed most recently comes first and new public repos show up on their own.
- **Featured project**: a Movie Gress card with a video player, plus a "NEW" badge in the hero.
- **Easter eggs**: a root mode with a small CTF, achievements, and a design mode for moving and resizing the page. Finding them is part of the fun.
- **Developer tools popup**: opening DevTools shows a joke alert in English or Bangla, with music. Right-click and the inspect shortcuts are blocked. This is for fun only; it doesn't really hide the code.
- **Contact form**: sends through Formspree and says so when a message fails.
- Responsive down to phone width, keyboard accessible, and respects reduced-motion settings.

## Running locally

The site fetches `music/playlist.json`, so serve the folder over HTTP instead of opening `index.html` directly:

```bash
git clone https://github.com/Xmon4u/xmon4u.github.io.git
cd xmon4u.github.io
python -m http.server 8080
```

Then open <http://localhost:8080>.

## Changing things

Everything is in `index.html`. The settings sit at the top of the main script; search for the heading in quotes to jump there.

| What | Where |
| --- | --- |
| Show or hide the "NEW" badge and the featured card, and change their text, link or video | `PROMO — CHANGE / HIDE` |
| Turn GitHub auto-sorting on or off, or hide a repo | `GITHUB — PROJECTS UPDATE THEMSELVES` (`hide: [...]`) |
| Replace a sound or change its volume | `SOUND FILES — CHANGE YOUR SOUNDS HERE` (see [`sounds/README.md`](sounds/README.md)) |
| Add or remove a hand-written project card | the `<section id="projects">` list |
| Add a music track | put the mp3 in `music/` and add an entry to `music/playlist.json` (`title` and `file`) |

## Folders

| Path | Contents |
| --- | --- |
| `index.html` | the whole site: HTML, CSS and JS in one file, no frameworks |
| `music/` | background tracks and `playlist.json` |
| `sounds/` | build and DevTools-popup sounds (generated for this site) |
| `video/` | the Movie Gress video |
| `avatar.jpg` | profile photo, also used for link previews |
| `.nojekyll` | tells GitHub Pages to serve the files as they are |

## Privacy

There are no analytics and no cookies. Two things talk to outside services:

- The project list calls the public GitHub API. The result is cached in the visitor's browser for an hour.
- The DevTools popup looks up the visitor's own IP address and city through GeoJS, and only shows it to that visitor. It only runs when the popup opens, and nothing is stored.
