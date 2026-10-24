# ArtViSiON — The Living Portfolio

Final GitHub Pages package: immersive 3D counter environment with five service islands, tablet catalogue, restored countertop accessories, brand red/silver finishes and transparent text labels (white text strips removed).

## Publish to the existing Counter repository

1. Extract this ZIP on your computer.
2. Open your `rjsarkar83/Counter` repository on GitHub. Back up your current website before replacing files.
3. Choose **Add file → Upload files**.
4. Upload the extracted files **directly into the repository root**, not inside an extra folder. Replace `index.html` with this version; include `app.js`, `style.css`, `three.js` and the license file. Keep any unrelated existing assets you still need.
5. Commit the upload.
6. In **Settings → Pages**, choose **Deploy from a branch**, your publishing branch (usually `main`), and **/(root)**. Save. If Pages is already configured this way, no setting change is needed.
7. After GitHub's deployment finishes, open `https://rjsarkar83.github.io/Counter/`. If the old design appears, hard-refresh or clear that site's cache.

No build step, npm install, API key or CDN is required. `.nojekyll` disables Jekyll processing. The old `?tab=3d` link also loads the main experience; query-based routing is not used in this replacement.

**This is a replacement homepage, not a merge with the old project's source.** Old kiosk pages, engineering sheets and external files are not included in this ZIP; preserve those in your repository if needed.

## Local preview

From this directory run:

```sh
python -m http.server 3000
```

Open `http://localhost:3000`. Do not open `index.html` using `file://`; browser module restrictions can prevent it from working.

## Features and controls

- Desktop: drag to orbit, wheel to zoom.
- Touch: drag to orbit, two-finger pinch to zoom.
- Select a division or click its island to focus the complete counter.
- Mobile: Tools opens the compact control panel.
- Tablet: click the physical screen or **Open touchscreen tablet** to browse services/products.
- **Explode all** separates the main counter, five islands, tablet, accessories and lighting. The separation slider adjusts spacing; Reassemble restores the saved positions.
- **Dimensions** opens measurement guides and a schedule. This mode returns the design to its assembled pose.
- `R`: reset; `+` / `-`: zoom; `1`–`5`: focus division; `Esc`: close dialog/panel.
- Cinema mode hides interface panels; press Escape to leave.

## Important notes

- Modern browser with WebGL and JavaScript required. Actual performance varies by device; an exhaustive physical-device/browser test has not been performed.
- JavaScript syntax was checked before packaging; relative local asset references were checked.
- All dimensions are nominal assembled 3D-model measurements, rounded to mm—not surveyed or fabrication-approved drawings. Exploded view is illustrative, not an engineered installation sequence.
- Services/products use representative concept miniatures, not one bespoke model for every catalogue entry. The original 21 product names have been restored. Each has a representative miniature in its division drawer and the main counter vitrine.
- The WhatsApp QR matrix and destination were restored from the supplied original page. Verify ownership/contact details before publishing. Target: `https://wa.me/919009001551?text=Hi%20RJ%2C%20I%20want%20to%20discuss%20a%20project.` Scanning opens WhatsApp; this site does not send messages automatically.
- Project forms download a local brief. No server submission or backend is provided.
- No GitHub deployment has been performed by the assistant; upload this package to publish it.

## Files

- `index.html` — entry page
- `style.css` — responsive interface
- `app.js` — geometry, camera, catalogue and interaction
- `three.js` — local Three.js 0.160.0 dependency
- `THREE-LICENSE.txt` — dependency license
- `.nojekyll` — GitHub Pages static-site marker

Original reference: https://rjsarkar83.github.io/Counter/

## Glass sample drawers update
All five circular display islands now have transparent glass drawers. Click the handle/front to slide a drawer outward; click again to close. Desktop drawer controls or mobile Tools also offer individual and open-all controls. Miniature geometry is illustrative, not manufacturing-detail CAD. The same original 21-product collection is also represented inside the five main counter vitrines.
