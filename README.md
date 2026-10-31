# QORA / Immersive Architecture Study

Original static immersive architecture concept with Three.js shader, Lenis scrolling, GSAP, cursor/touch interaction, loading sequence, navigation, and an original locally bundled ambient audio loop. This is not a copy of Immersive Garden's code or proprietary artwork.

## Preview

Run `python3 -m http.server 8080` from this folder and visit `http://localhost:8080`. Requires network access to load Three.js, GSAP, Lenis and Howler from esm.sh.

## Publish on GitHub Pages

Upload `index.html` and `assets/` to repository root, enable Settings > Pages > Deploy from branch > main / root. Live URL is created by GitHub, not included here.

## Important release checks

The WebGL shader has not been verified across real browsers or mobile devices in this environment. Dependencies currently load from CDN. Verify WebGL, scrolling, audio autoplay restrictions, mobile performance, and accessibility. The CTA uses placeholder `hello@qora.studio` and **must be replaced with an approved contact** before production. The relief is procedural rather than a photogrammetry-derived architectural 3D model.

## Validation performed (2026-10-31)
- JavaScript module passed Node.js syntax check.
- ZIP archive passed CRC/integrity validation.
- Bundled MP3 was recognized as MPEG audio.
- Unapproved placeholder email removed from the CTA.
- Automated Chromium screenshot attempt timed out; visual/browser/mobile testing remains outstanding.
- No public deployment has been performed.
