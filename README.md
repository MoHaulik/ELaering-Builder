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

- Upload 360°/180° videos and images
- Text overlays, multiple-choice interactions, timed appearance, formatting
- Save / reload a project (`.lxr`), export a finished scenario as a single `.zip`

The exported `.zip` contains `project.json` plus `videos/` and `images/` — the
package the **Player** reads.

## Dependencies

Vendored — this page loads nothing from a third-party CDN.

| File | Version | License |
| --- | --- | --- |
| `vendor/jszip.min.js` | JSZip 3.10.1 | MIT / GPLv3 |
