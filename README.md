# Tappy-Plane

A fast, one-tap arcade flyer that runs in any browser — no install, no build step, no dependencies. Tap to climb, dodge the rocks, grab the stars, and see how far you can fly.

**[▶ Play it live](https://YOUR-USERNAME.github.io/YOUR-REPO/)** *(replace with your GitHub Pages link)*


## About

Tappy Plane is a mobile-first HTML5 canvas game in the spirit of the classic "tap to flap" genre. It is a single self-contained `index.html` file: the code and every sprite are embedded, so it works offline and deploys anywhere static files can be hosted.

## Features

- **One-tap controls**: tap, click, or press Space / ↑ to flap
- **Mobile responsive**: the view adapts to any screen size, portrait or landscape, and stays sharp on high-DPI displays
- **Collectible stars**: each star adds to your score, on top of every rock you pass
- **Four plane colors**: yellow, green, blue and red, chosen from the start screen and remembered between visits
- **Changing scenery**: every 10 points the ground and rocks switch between grass, dirt, snow and ice
- **Medals**: earn bronze (10), silver (20) and gold (30) on the game-over panel
- **Best score saved** locally in your browser
- **Polish**: animated propeller, smoke trail, screen shake on crash, pulsing tap hints

## How to play

| Action | Control |
| --- | --- |
| Start / flap | Tap, click, Space or ↑ |
| Pick a plane | Tap a plane on the start screen |
| Retry | Tap after the game-over panel appears |

Fly through the gaps between the rocks. Touching a rock, the ground, or the top of the screen ends the run.

## Run locally

No tooling needed. Either open the file directly:

```bash
open index.html
```

or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Push `index.html` to the root of your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After a minute, your game is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

## Tech

- Plain HTML, CSS and JavaScript
- HTML5 `<canvas>` rendering with a fixed logical height that scales to the screen
- `requestAnimationFrame` game loop with frame-time clamping
- `localStorage` for best score and plane color, wrapped in `try/catch` so the game still works when storage is blocked

## Customize

Everything lives in `index.html`. Useful constants near the top of the script:

| Constant | What it does |
| --- | --- |
| `SP` | Scroll speed |
| `DIST` | Distance between obstacles |
| `GH` | Ground height |
| gravity / flap values in `update()` and `flap()` | How floaty or heavy the plane feels |
| `THEMES` | Which rocks and ground appear for each scenery |

## Credits

Art assets are from **[Kenney](https://kenney.nl)** and released under **CC0 1.0 (public domain)**. Attribution is not required, but it is much appreciated. Consider supporting Kenney at [kenney.nl](https://kenney.nl).

## License

Code: MIT. See `LICENSE`. Art: CC0 by Kenney.


*Made with HTML5 canvas and a lot of tapping.*
