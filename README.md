# OBSERVATORY — Architecture in Presence V10

A self-contained static architectural interactive concept. Open through an HTTP server (e.g. `python3 -m http.server 8000`) or publish the entire folder to a static host.

## Interaction
- Scroll: facade starts flat, extrudes according to the supplied approximate depth map, then rotates in perspective with a close approach.
- Pointer: local subtle refraction near the cursor only; camera does not follow the pointer.
- Sound: opt-in via Sound button.
- Reduced motion: original photograph.

## Limitations
This is a single-view photographic 2.5D relief, not an exact architectural 3D reconstruction. Hidden building sides cannot be inferred from the source photograph. The photographic asset requires rights clearance before commercial deployment. Mac M4/Safari performance must be verified on actual hardware.
