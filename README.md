# Orbis UI — PS5-inspired dashboard concept

Orbis UI is a responsive, controller-friendly dashboard concept inspired by the visual language of modern console home screens. It is an independent web project, not Sony system software.

## Run it
- Open `index.html` in a modern browser for a local preview.
- For offline caching and install support, serve it from HTTPS (for example, GitHub Pages). Service workers do not run from a `file://` address.
- No framework, package manager, or build step is required.

## Features
- Responsive home screen with selectable game/app tiles.
- Control Centre with saved demo toggles for Network, Sound and Microphone.
- Settings with saved accent colour and reduced-motion preference.
- Editable local display profile.
- Keyboard, touch/click and standard browser Gamepad API navigation.
- Installable PWA manifest and service-worker cache for supported browsers.
- GitHub Actions workflow for basic JavaScript and project-file checks.

## Controls
| Input | Action |
|---|---|
| D-pad / left stick | Navigate |
| Cross / Enter | Select |
| Circle / Escape / Backspace | Back |
| Options / M / F1 | Control Centre |
| L1 / R1 | Previous / next tile |

Controller button indices can vary by browser and controller. The PS button is reserved by the console and is not reliably exposed to web pages.

## PS4 integration: what is and is not possible
This project can run as a webpage in the PS4 browser, subject to browser compatibility. It cannot:
- Replace the PS4 system shell or appear as the actual console home screen.
- Globally intercept or remap the PS button.
- Automatically enumerate or launch installed PS4 games.
- Change firmware, impersonate PS5 hardware, or provide genuine PSN functions.
- Run PS5 games or turn PS4 hardware into PS5 hardware.

Those functions require privileged platform-level integration and cannot be achieved by adding JavaScript to a webpage. This project does not spoof console identity or bypass Sony authentication.

## Project structure
- `index.html` — page structure and PWA metadata.
- `styles.css` — responsive visual design.
- `app.js` — interactions, settings and controller support.
- `manifest.webmanifest` — install metadata.
- `sw.js` — offline asset cache.
- `.github/workflows/validate.yml` — lightweight repository checks.

## Hosting
Enable GitHub Pages for the repository's `main` branch and root folder. Once published, open the Pages URL in a supported browser. The PWA install prompt is browser-dependent; the PS4 browser does not gain native shell privileges from installing or hosting this page.

## Licence and assets
The interface uses original code, gradients and generic placeholder artwork. It does not include Sony system files, proprietary game assets or PlayStation trademarks beyond descriptive references.
