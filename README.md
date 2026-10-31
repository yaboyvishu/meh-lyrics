# Constellation Lyrics

Animated lyrics for any song. Each word becomes a glowing star as it is sung, linked to the one before it, in the style of the "constellation" lyric reels. Runs entirely in the browser, with no build step and no server.

Made by **vishumadethis**.

## Features

- Constellation and Web styles with eased motion, ripples and a smooth fade-out trail
- Synced lyrics fetched from [LRCLIB](https://lrclib.net) automatically, or paste your own LRC
- Live sync offset slider (-2000 to +2000 ms) and a glow slider
- Color presets and custom pickers for stars, active word and background
- Free Creative Commons music search through [Jamendo](https://developer.jamendo.com)
- Fullscreen mode (F key, double-click, or button), Space to play or pause
- Record the animation with audio to a .webm video
- Responsive layout that works on phones

## Run locally

Open `index.html` in Chrome or Edge. That's it.

## How to use

1. Pick a song file, or search free music in the Jamendo section.
2. The lyrics search runs automatically from the file name. Pick another match from the list if needed.
3. Press play. If the words feel early or late, move the **Sync offset** slider.
4. Choose a style and colors, then use **Record video** or go fullscreen.

### Jamendo client ID

The free music search needs a free client ID from <https://developer.jamendo.com>. Paste it in the Jamendo section once. It is stored in your own browser only (localStorage) and never sent anywhere except Jamendo.

## Deploy to Vercel

1. Push this folder to a GitHub repository.
2. Go to <https://vercel.com/new> and import the repository.
3. Set the framework preset to **Other**. Leave the build command and output directory empty.
4. Click **Deploy**.

Or with the CLI: `npm i -g vercel`, then run `vercel --prod` in this folder.

## Notes

- Lyric timing inside each line is estimated by word length. Line timing comes from the LRC file.
- Recording captures the animation only (not the page watermark). If audio comes out silent for a Jamendo track, use Win+Alt+R (Xbox Game Bar) instead.
- The font is subset to Latin characters. Lyrics in other scripts fall back to a system font.
- iPhone Safari does not support fullscreen on this element, so the fullscreen button is hidden there.

## Credits and licenses

- Code: MIT, see `LICENSE`
- Font: Google Sans Bold, SIL Open Font License 1.1, see `fonts/OFL.txt`. A Latin subset is embedded in `index.html`.
- Lyrics: provided by LRCLIB under its own terms
- Music search: Jamendo tracks are Creative Commons. Credit the artist if you post a video.
