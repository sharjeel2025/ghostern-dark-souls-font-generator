# Dark Souls Font Generator

A vanilla JS/Canvas tool that recreates Dark Souls' in-game typography —
"YOU DIED" screens, boss banners, death messages — as downloadable PNGs.
No frameworks, no build step, runs entirely client-side.

**[Live demo →](https://ghostern.com/gaming/fonts/dark-souls/)**

## Why I built this

Every "YOU DIED" generator I found online used the wrong font or added a
watermark. I studied the game's actual UI typography and rebuilt it from
scratch using the [Canvas 2D API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) —
no WebGL, no dependencies, so it runs fast even on low-end devices.

## How it works

- Text rendering uses [Cinzel](https://fonts.google.com/specimen/Cinzel), the closest open
  license match to the game's modified serif typeface (per the [Dark Souls Wikipedia
  entry](https://en.wikipedia.org/wiki/Dark_Souls) on the game's visual design)
- Glow effect: layered `shadowBlur` passes on an offscreen canvas, not a CSS filter,
  so it exports correctly to PNG
- Background compositing: opacity-blended image layer behind text, with an
  aspect-ratio-fit function for portrait/mobile wallpaper exports

## Run it locally

No build tools needed — just open `index.html` in a browser, or:

\`\`\`bash
git clone https://github.com/sharjeel2025/ghostern-gaming-text-tools
cd ghostern-gaming-text-tools
python3 -m http.server 8000
\`\`\`

## Tech stack

Vanilla JavaScript, HTML5 Canvas, CSS3 — deliberately no frameworks or build
tools, so anyone can read the source top to bottom.

## Live version

The maintained, full-featured version (more fonts, backgrounds, and presets)
runs at [ghostern.com](https://ghostern.com/gaming/fonts/dark-souls/) — this repo
is the open-source core of that tool.

## License

MIT — use it, fork it, ship it.

## Author

Built by [Sharjeel](https://ghostern.com/about/) — I build free gaming tools
at [Ghostern](https://ghostern.com).
