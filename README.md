# BioSound AI — Sound-Ai-v2.2

Android-friendly live environmental sound recognition and frequency display.

## GitHub Pages
Keep `index.html`, `manifest.webmanifest`, `sw.js`, and `icon.svg` in the repository root. The workflow in `.github/workflows/pages.yml` deploys on pushes to `main`. In repository **Settings → Pages**, choose **GitHub Actions** as the source. When deployment completes, open `https://OWNER.github.io/REPOSITORY/`.

## Android
Open the HTTPS Pages URL in Chrome, allow microphone permission, tap **Start listening**, and optionally choose Chrome → ⋮ → Add to Home screen.

## Features
- Google YAMNet environmental audio classifier via MediaPipe Tasks Audio.
- Top sound label and up to four alternatives.
- Live frequency spectrum, dominant-frequency estimate, and RMS level.
- Microphone audio is processed in the browser; this app does not upload or save recordings.

## Limitations
- YAMNet is a general environmental sound classifier, not a custom model for every appliance or vehicle.
- Scores are not calibrated probabilities.
- Internet is needed to load MediaPipe and YAMNet. The service worker caches the app shell only.
- This is a PWA, not a native APK, and has not yet been tested on the user's phone.
- Insect species identification is not included in this baseline.
