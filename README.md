# Orbis UI — PS5-inspired dashboard concept

Orbis UI is a responsive, controller-friendly dashboard concept inspired by modern console home screens. It is an independent web project, not Sony system software.

## Run the web version
- Open `index.html` in a modern browser for a local preview.
- For offline caching and browser install support, serve it from HTTPS (for example, GitHub Pages). Service workers do not run from a `file://` addresses.
- The web version has no build step or frontend framework.

## Android companion
A Capacitor wrapper is included to package the same dashboard as a normal Android app. It is a companion app, not a PS4 firmware app or system-menu replacement.

- GitHub Actions can build a debug APK using **Actions → Build Android companion APK → Run workflow**.
- Download the resulting `orbis-ui-android-debug` artifact from that workflow run.
- The APK is a debug build for testing; it is not a Play Store release.

## Features
- Responsive home screen with selectable game/app tiles.
- Control Centre with saved demo toggles for Network, Sound and Microphone.
- Settings with saved accent colour and reduced-motion preference.
- Editable local display profile.
- Keyboard, touch/click and standard browser Gamepad API navigation.
- PWA manifest and service-worker cache for supported browsers.
- Capacitor Android companion wrapper and automated APK build workflow.
- GitHub Actions checks for JavaScript syntax and required project files.

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
This project can run as a webpage in the PS4 browser, subject to browser compatibility. The Android wrapper can run on Android devices. Neither can:
- Replace the PS4 system shell or appear as the actual console home screen.
- Globally intercept or remap the PS button.
- Automatically enumerate or launch installed PS4 games.
- Change firmware, impersonate PS5 hardware, or provide genuine PSN functions.
- Run PS5 games or turn PS4 hardware into PS5 hardware.

Those functions require privileged platform-level integration and cannot be achieved by adding JavaScript or wrapping it in an Android app. This project does not spoof console identity or bypass Sony authentication.

## PS4 firmware research
See [PS4 firmware 14.02 compatibility notes](docs/PS4-14.02-compatibility.md). The project currently treats 14.02 homebrew runtime compatibility as unverified; compiling an application is not proof that it can run on a particular console.

## Project structure
- `index.html` — page structure and PWA metadata.
- `styles.css` — responsive visual design.
- `app.js` — interactions, settings and controller support.
- `manifest.webmanifest` and `sw.js` — install metadata and offline cache.
- `capacitor.config.json`, `package.json` — Android wrapper configuration.
- `scripts/copy-web.js` — prepares web assets for Android.
- `.github/workflows/` — validation, Pages deployment and Android APK build workflows.
- `docs/ROADMAP.md` — practical next stages and platform boundaries.
- `docs/PS4-14.02-compatibility.md` — firmware research and verification plan.

## Hosting the web version
The repository includes a GitHub Pages deployment workflow. In repository **Settings → Pages**, set the build/deployment source to **GitHub Actions**. The workflow will then publish the static site after a push to `main`. The PWA install prompt is browser-dependent; the PS4 browser does not gain native shell privileges from hosting or installing this page.

## Licence and assets
The interface uses original code, gradients and generic placeholder artwork. It does not include Sony system files or proprietary game assets.
