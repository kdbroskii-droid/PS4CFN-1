# Orbis UI roadmap

## Shipped in the web prototype
- Responsive console-style dashboard.
- Keyboard, touch and browser Gamepad API navigation.
- Control Centre, settings and local profile.
- Persistent local preferences.
- PWA manifest and offline service-worker cache.
- Automated JavaScript syntax and required-file checks.
- GitHub Pages deployment workflow.

## Next practical stages
1. **Publish and test:** enable GitHub Pages with the GitHub Actions source, then test the published URL on the PS4 browser and Android.
2. **Controller compatibility:** record the actual browser Gamepad API button mapping for each connected controller. The mapping is browser/controller dependent.
3. **Native Android companion:** package the same web interface in an Android app shell if a standalone APK is wanted. This would still be a companion dashboard, not a PS4 system replacement.
4. **Optional local network companion:** build a separate phone/PC companion for displaying status and providing user-triggered shortcuts. It must use supported console interfaces; it cannot gain privileged access to PS4 system functions.

## Platform boundary
A normal web page or Android wrapper cannot become the PS4 system shell, receive the reserved PS button globally, enumerate installed games, launch games through private system APIs, or alter console identity. Those are platform-level capabilities, not missing frontend features. Do not treat browser APIs or a PWA as a firmware integration mechanism.
