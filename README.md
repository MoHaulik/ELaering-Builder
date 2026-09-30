# E-Læring — Builder

Browser-based authoring tool for 360°/180° VR training scenarios, built for the
Meta Quest 3. Open `index.html` in any modern browser — no build step, no install,
no server requirement beyond static file hosting.

An independent client product ("E-Læring"), built to the requirements in
*Kravspecifikation til VR-scenarie byg editor v0.8*.

## Key features

- **Visual identity.** Stylish black-and-white chrome (monochrome buttons,
  borders and panels). Functional colour is kept only where it carries meaning in
  the node graph — the green "start" marker and correct/incorrect answer paths, and
  red for destructive actions.
- **No Dashboard module.** This product ships as Builder + Player only.
- **Access-code gate (spec req. ID:02_07).** An "Access code" field in the
  header is written into the exported `project.json`. If set, the Player requires
  that exact code before a scenario can start. There is no remote-start or relay
  system — every run is fully local (see the Player README).

## What this module does

- Upload 360°/180° videos, plus images and flat video clips (the **Media** tab)
- **POV preview** in every scene: the real clip in perspective, drag to look
  around, zoom, a timeline to scrub, and drag-and-drop placement of waypoints,
  texts, media and the question (files can be dropped straight onto the view)
- Waypoints anywhere in 360°, optionally lying flat on the floor
- Trim, fade in/out, start direction ("Set start view here"), smooth/direct cuts
- Full preview from the selected scene / from a point in time / one scene only
- Compression with quality presets, progress bar and before/after comparison
- Work (including media files) is kept automatically in this browser
  (IndexedDB) — nothing is uploaded. Export a `.zip` to back up or move to
  another computer, and open it again with the folder icon.

The exported `.zip` contains `project.json` plus `videos/` and `images/` — the
package the **Player** reads.

## Dependencies

Vendored — this page loads nothing from a third-party CDN.

| File | Version | License |
| --- | --- | --- |
| `vendor/jszip.min.js` | JSZip 3.10.1 | MIT / GPLv3 |
| `vendor/three.min.js` | three.js r150 (same file as the Player's) | MIT |
