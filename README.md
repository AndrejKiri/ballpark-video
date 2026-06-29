# ballpark-video

Two-page GitHub Pages site hosting UI refresh preview videos. Each option lives on its own URL with a single fullscreen video and playback controls.

## Live URLs

- **Index** (links to both): https://andrejkiri.github.io/ballpark-video/
- **Option A**: https://andrejkiri.github.io/ballpark-video/a/
- **Option B**: https://andrejkiri.github.io/ballpark-video/b/

## Structure

```
.
├── index.html        # Landing page linking to A and B
├── a/index.html      # Option A — single video
├── b/index.html      # Option B — single video
├── videos/
│   ├── option-a.mp4
│   └── option-b.mp4
└── .nojekyll         # Serve files as-is, skip Jekyll processing
```

## Playback behaviour

Videos load paused with native controls — the viewer presses play, with sound. No autoplay, no loop. To change behaviour, edit the `<video>` tag attributes in `a/index.html` / `b/index.html`:

- `autoplay muted` — play automatically on load (browsers require `muted` for autoplay)
- `loop` — repeat after finishing

## Deployment

Served by GitHub Pages from the `main` branch root. Push to `main` and Pages rebuilds automatically (~1 min).
