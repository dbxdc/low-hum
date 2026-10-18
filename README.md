# Low Hum

A bedside sleep-sound generator. Everything is synthesized live in the browser with the Web Audio API, so there are no recordings and no audible loop.

## What it plays

- **Brown noise** – the main layer; energy falls 6 dB per octave for a deep, even roar.
- **Sub rumble** – brown noise filtered below 80 Hz.
- **Pink noise** – a brighter layer for masking voices and traffic.
- **Warmth** – a low-pass filter that sweeps from 4.5 kHz down to 250 Hz.
- **Slow swell** – an optional rise and fall at 0.1 Hz (six cycles a minute).

Presets: Deep brown, Cabin hum, Slow tide, Soft blend. A sleep timer (30, 60, 90 minutes or all night) fades out over the last three minutes.

## Files

- `index.html` – the whole app: markup, styles and script in one file.

## Using it on an iPhone

Open `index.html` in Safari, turn off the ring/silent switch, and keep the page open while it plays. Headphones or a Bluetooth speaker reproduce the low rumble far better than the phone's speaker.
