# Low Hum

A bedside sleep-sound generator. Everything is synthesized live in the browser with the Web Audio API, so there are no recordings and no audible loop.

## What it plays

- **Brown noise** – the main layer; energy falls 6 dB per octave for a deep, even roar.
- **Sub rumble** – brown noise filtered below 80 Hz.
- **Pink noise** – a brighter layer for masking voices and traffic.
- **Warmth** – a low-pass filter that sweeps from 4.5 kHz down to 250 Hz.
- **Slow swell** – an optional rise and fall at 0.1 Hz (six cycles a minute).
- **Soften the roar** – cuts up to 12 dB around 220 Hz and 6 dB around 700 Hz, the band that makes noise sound like an engine.
- **Drift** – three slow oscillators (37, 61 and 97 second periods) gently vary the tone and level so the sound never feels mechanical.

Presets: Calm night (default), Hush, Deep brown, Slow tide, Soft blend, Cabin hum. The sound fades in over 30 seconds. A sleep timer (30, 60, 90 minutes or all night) fades out over the last three minutes.

## Files

- `index.html` – the whole app: markup, styles and script in one file.
- `sw.js` – service worker that saves the app on the device so it opens offline. Bump `VERSION` whenever the app files change.
- `manifest.webmanifest` – name, colors and icons for "Add to Home Screen."
- `icons/` – Home Screen icons.

## Offline use

The site is published with GitHub Pages at https://dbxdc.github.io/low-hum/. Open it once in Safari while online, tap Share → Add to Home Screen, then launch it from the icon. After that first visit it works in airplane mode.

## Using it on an iPhone

Open `index.html` in Safari, turn off the ring/silent switch, and keep the page open while it plays. Headphones or a Bluetooth speaker reproduce the low rumble far better than the phone's speaker.
