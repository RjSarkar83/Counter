# Performance & browser QA

## Changes
- Consolidated 266 static miniature sub-meshes through material-based geometry batching.
- Shared miniature materials and added distance-based simplified geometry; close/selected products retain detailed models.
- Balanced mode disables expensive realtime shadows. Detail mode can enable shadows on non-compact devices.
- Capped render resolution by device class; Smooth mode reduces rendering resolution further.
- One animation loop replaces independent camera/logo loops.
- Pauses 3D rendering while service/design tabs or modal catalogues cover the scene, and while the page is hidden.
- Background rendering is throttled in selected-counter isolation; the sharp foreground continues updating.
- Skips inactive assembly and dimension work, debounces search and reduces CSS blur cost.
- Responsive scrollable right dock and mobile tools sheet replace overlapping panels.
- Fixed persistent dimension labels after closing measurement mode.
- Versioned CSS and app URLs help prevent mixed old/new assets after deployment.

## Automated checks
Chromium headless with software WebGL, emulated viewport/touch configurations:

| Viewport | Runtime/console errors in tested flow | Horizontal page overflow | Focus, drawer, catalogue, explode, dimensions |
|---|---|---|---|
| Desktop 1440 × 900 | 0 | No | Passed |
| Mobile 390 × 844 | 0 | No | Passed |
| Tablet 820 × 1180 | 0 | No | Passed |
| Landscape 844 × 390 | 0 | No | Passed |

The test opened a counter, reset the view, opened a main-counter drawer, opened the tablet, checked a no-results search, closed the tablet, exploded/reassembled, opened/closed dimensions and returned to the showroom. Catalogue pause state was also verified. Some controls were activated programmatically for repeatable tests; this is not exhaustive gesture/hit-target validation.

## Performance interpretation
30 FPS on compact devices and 45 FPS on desktop are scheduling targets in balanced mode, NOT measured or guaranteed frame rates. Smooth mode targets 24 FPS; Detail mode targets 60 FPS. Software-rendered sandbox testing cannot predict actual GPU performance on a phone.

Model count remains substantial. Select Smooth under Graphics on lower-powered devices. Real Safari/iOS/Android hardware, thermal/battery performance and all possible input gestures have not been exhaustively tested. A modern WebGL-capable browser is required.

## Original restoration verification
After the source restoration, Chromium desktop (1440×900) and touch/mobile (390×844) checks verified all five original sample files loaded, original Screen UI mounted, and catalogue totals were 28 services / 216 items / 21 products. No runtime/console errors were reported in those tested flows. The original-source challenge-script 404 was removed before the final rerun.
