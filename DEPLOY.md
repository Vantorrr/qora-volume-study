# Run and publish

## Local preview
From this directory run:

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080` in Chrome or Safari. A connection to `esm.sh` is needed for the WebGL-enhanced version. If unavailable, the page uses the built-in Canvas 2D depth fallback.

## Static hosting
Upload `index.html` and the complete `assets/` directory to any static hosting service, preserving paths. Configure HTTPS and serve `index.html` at the root. No server-side code is required. Do not publish publicly with the current photo until its licensing is verified.

## Replace the reference photograph
Supply a licensed or client-owned landscape photograph, update `assets/hero.jpg`, and create a new aligned grayscale `assets/depth.png` at the same aspect ratio (white = nearer). Review framing and geometry after replacement. The existing depth map is not transferable to a different photograph.

## Acceptance checklist
- Desktop and mobile scroll and photo/depth alignment
- WebGL console and GPU support on target browsers
- Touch and keyboard accessibility, reduced-motion settings
- Audio starts only after interaction
- Copyright permission for all visual assets
- Performance and Lighthouse checks on actual hosting
