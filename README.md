# Scroll Walk

A scroll-driven character animation. As you scroll down the page a character walks forward, pauses to face you when you change direction, then walks back the way they came when you scroll up.

## How it works

- Built with vanilla HTML, CSS, and Canvas API — no frameworks or build tools required.
- Sprite sheet frames are pre-rendered into off-screen canvases with automatic center-of-mass correction to eliminate drift.
- Scroll direction is tracked in real-time; a configurable threshold (`FACING_THRESHOLD`) controls how long the character holds the facing pose before walking in the new direction.
- Frame rate is capped (`MIN_MS_PER_FRAME`) so the walk cycle always looks natural regardless of scroll speed.

## Assets

| File | Description |
|---|---|
| `scroll-walk.html` | Main page — all code is self-contained |
| `Character4.png` | 8-frame horizontal walk cycle sprite sheet (4728×817) |
| `Facing-01.png` | Single idle/facing frame shown on load and direction changes |

## Running locally

```bash
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080).

## Deploying to Vercel

1. Push this repo to GitHub.
2. Go to [vercel.com](https://vercel.com), click **Add New Project**, and import the repo.
3. Leave all settings as default — Vercel will detect it as a static site.
4. Click **Deploy**.
