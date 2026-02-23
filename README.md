# QRTOY

Rapid-fire mobile QR scanner with instant URL loading.

## What It Is

QRTOY is a single-page web app optimized for portrait mobile use:
- Top area: embedded browser (`iframe`) for scanned URL targets
- Bottom area: live camera scanner with continuous QR detection

## Core Behavior

- Continuously scans QR codes in the visible camera viewport
- Loads valid `http/https` QR URLs immediately in the top frame
- Shows a startup message until the first successful scan
- Detects duplicate scans of the current URL and shows a reload CTA after 2 seconds
- Supports camera switching and zoom controls
- Gives scan feedback with a brief flash + shutter sound when a new load starts

## Languages

UI text is localized via local `i18n.json` (no online translation service), currently:
- English
- German
- French

## Browser Notes

- Camera access requires a secure context (`https` or `localhost`)
- Uses native `BarcodeDetector` when available
- Falls back to `jsQR` for browsers (including many iOS/WebKit cases) without native QR detection

## Files

- `index.html`: complete app UI + scanner logic
- `i18n.json`: localizable text resources

## Author

ChatGPT with Max Wolf / MESO
