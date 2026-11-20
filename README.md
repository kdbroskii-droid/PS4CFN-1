# Orbis UI — PS5-inspired dashboard prototype

A responsive browser-based dashboard inspired by the PS5 home screen. It is a front-end concept and does not replace or modify the PS4 system software.

## Run
Open `index.html` in a modern browser. The project is split into `index.html`, `styles.css` and `app.js`; no build step or dependencies are required.

## Included
- PS5-inspired home screen with game tiles.
- Control Centre overlay with interactive Network, Sound and Microphone demo toggles.
- Settings panel with saved accent colour and reduced-motion preference.
- Editable local profile saved in browser storage.
- Game Library, Store and Notifications preview panels.
- Keyboard, touch/click and standard browser Gamepad API navigation.

## Controls
- D-pad / left stick: navigate tiles.
- L1 / R1: jump backward / forward through the game tiles.
- Cross / Enter: select.
- Circle / Escape / Backspace: back.
- Options / M: open Control Centre (controller mapping varies by browser).
- Touchpad click may map to a browser gamepad button on some devices.

## Important PS4 limitations
- A browser page cannot replace the PS4 system shell or globally intercept the PS button.
- The PS button is reserved by the console/browser and is not reliably exposed through the browser Gamepad API. Therefore PS tap = Control Centre and PS hold = Home cannot be implemented globally in this web prototype.
- A normal web page cannot launch installed PS4 games, enumerate the installed game library, change firmware, spoof PS5 hardware identity, or provide PSN account functions.
- The local profile is only a dashboard display name, not a genuine PSN account.
- This project does not bypass Sony authentication or modify console identity.

The interface uses original code and generic placeholder artwork, not Sony system software or proprietary assets.
