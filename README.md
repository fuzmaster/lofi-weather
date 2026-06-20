# Lofi Weather

A retro Weather Channel-style web app — CRT styling, auto-cycling forecast "channels," and a built-in lofi music player. Inspired by [weather.com/retro](https://weather.com/retro) and [WeatherStar 4000+](https://weatherstar.netbymatt.com/).

Single static HTML file. No build step, no API keys, no server.

## Features

- **Live weather** via [Open-Meteo](https://open-meteo.com/) (free, no key)
- **4 auto-cycling channels**: Current Conditions, Hourly, 7-Day, Almanac
- **CRT styling**: scanlines, vignette, scrolling ticker crawl
- **Music player** with SomaFM streams (Groove Salad, Drone Zone, Lush, Fluid, Deep Space One), Lofi Girl, and a custom YouTube playlist field
- **32-bar procedural audio visualizer**
- **6 color themes**: Classic (yellow/blue), Vapor, Forest, Sunset, Mono, Ocean
- **Settings persist** to localStorage — location, units (F/C), brand name, cycle speed, channels, theme, crawl message, station, volume

## Run locally

Just open `index.html` in a browser. Or serve it:

```bash
python -m http.server 8000
# or
npx serve .
```

## Deploy

Drop the repo into Vercel, Netlify, Cloudflare Pages, or GitHub Pages — it's a static site, no config needed.

## Customize

Click the ⚙ button (top-right) to set:

- **Location** — city name, ZIP, or `lat,lon`
- **Brand Name** — replaces "LOFI WEATHER" in the header
- **Units** — Fahrenheit/mph or Celsius/km/h
- **Cycle Speed** — seconds per channel
- **Channels** — toggle which forecast pages appear
- **Theme** — six built-in palettes
- **Crawl Message** — text in the scrolling ticker
- **Custom YouTube Playlist** — paste a video URL, playlist URL, or playlist ID; then pick "Custom YouTube" in the station menu

## Notes

- Browsers block autoplay with sound, so click ▶ on the player once per session.
- YouTube audio can't be analyzed cross-origin, so the visualizer is procedural (not a real FFT). Looks the same.
- SomaFM streams are free and listener-supported — [consider donating](https://somafm.com/support/).

## License

MIT.
