# Site sounds

| File | When it plays |
| --- | --- |
| `build-music.mp3` | Loops while the site builds (first visit, or Ctrl+K → "New build") |
| `build-done.mp3` | Once, when the build finishes |
| `devtools-alarm.mp3` | Alarm when developer tools are detected |
| `devtools-music.mp3` | Loops while the "Developer Tools Detected" popup is open |

## Changing a sound

- **Easiest:** replace the file with your own and keep the **same name** (e.g. save your track as `devtools-music.mp3`).
- **Different name or format:** open `index.html`, search for `SOUND FILES — CHANGE YOUR SOUNDS HERE`, and change the path in `SOUNDS`. mp3, ogg, wav and m4a all work.
- **Volume:** change the matching number in `SOUND_VOL` right below it (0 = silent, 1 = full).
- **Turn one off:** set its path to `''`.

The default files are original sounds generated for this site, so they're free to use.
