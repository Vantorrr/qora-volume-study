# Observatory — architectural photo + depth study

Open via a local web server (e.g. `python3 -m http.server 8080`), then http://localhost:8080. The photo fallback works without CDN, but the WebGL scene uses Three.js, GSAP, Lenis and Howler from esm.sh and requires internet. Do not open the file directly if you need reliable module and asset loading.

## Assets
- `assets/hero.jpg`: actual photograph of an observatory-like building, taken from a bundled unverified archival LaTeX template asset (`uantwerpendocs/Images/uantwerpen-01.jpg`). **Rights have not been independently verified**; for private concept evaluation only. Replace before public/commercial launch with client-owned/licensed material.
- `assets/depth.png`: artist-directed, approximate grayscale depth map created for THIS photograph. White=foreground; dark=background. It is not true measured depth.
- `assets/ambient.mp3`: original ambient drone generated for the prototype.

## Important limitations
This is a **real photograph**, not a procedural illustration, but it is **not Sagrada Família**, nor a full 3D model. Geometry is a single subdivided plane displaced by a hand-authored depth map; it does not recreate occluded surfaces. The reference photograph and map must be replaced with client's assets for delivery. No claims of client association or rights.


## Robustness update
The main page includes an inlined Canvas 2D depth renderer that starts if CDN imports or WebGL initialization fail. It uses the actual `assets/hero.jpg` and `assets/depth.png` rather than an abstract shader. This fallback is interactive but less physically accurate than WebGL. For commercial deployment, replace the reference photograph with client-owned/licensed assets and validate in a browser.

## Browser validation (31 October 2026)
The actual Chromium engine was used through Playwright with the HTML and image assets embedded into the test page to bypass restrictions on local file/HTTP navigation. For this isolated **Canvas fallback** test, CDN imports were deliberately disabled. Screenshots at 1440x900 and 390x844 were reviewed; image/depth rendered, the scroll-progress value changed, the headline faded, the sound control toggled, and no JavaScript page errors or mobile horizontal overflow were observed. This **does not validate the Three.js WebGL path**, external CDN loading, or the real site's HTTP deployment.

The demo remains an evaluation study, not a production release. The photograph's license is unverified, and the scene has not been evaluated against the client's actual photographs.

## Revision V2 — cursor and performance
- Added seven-point smoothed cursor trail to the WebGL photo-displacement shader.
- Added an independent, resolution-capped 2D canvas cursor-displacement fallback when WebGL cannot initialize.
- Render loop caps approximate GPU frame rate and internal resolution; reduced-motion preference preserves static photograph.
- Tested Chromium page rendering via embedded assets at desktop 1440×900 and mobile 390×844: canvas active, no JavaScript exceptions, no horizontal overflow. This is not an M4/Safari performance certification.
- The photographic stand-in does not have verified redistribution/commercial licensing. Replace with client-owned or appropriately licensed image before commercial publishing.
