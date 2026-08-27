# ATQ
A calm, low-stimulation speech &amp; OT therapy app for kids with ASD — built as a personal family tool, no accounts or data collection.
# Star Path 🦊

A calm, low-stimulation speech and occupational therapy app, built as a personal family
tool for two boys (ASD Level 2). It exists as an alternative to television, YouTube, and
mainstream gaming apps that tend to be either overstimulating or too complex — while still
giving the kids something on a screen they genuinely enjoy engaging with.

Single self-contained web app. No accounts, no ads, no analytics, no data collection.

## Activities

| Tile | Skill focus | Notes |
|---|---|---|
| 🗣️ Sound Out | Articulation | Picture/word cards, hear-it + say-it practice, capped replays |
| 💬 Word Builder | Expressive language | Tap-to-build sentences from a picture; each word usable once |
| 📋 First, Then | Sequencing / following directions | Watch-the-order demo, then errorless practice — wrong slots simply refuse the piece |
| ✏️ Trace It | Fine motor | Finger-tracing with a forgiving tolerance; ink only draws near the guide shape |
| 🌿 Calm Corner | Self-regulation | Breathing exercise, silent "Quiet Sort" (designed for use with ear defenders), bubble pop |
| 🎲 Take Turns | Social / turn-taking | Two-player emotion-matching memory game |
| 📸 Photo Hunt | Real-world vocabulary | Camera + on-device AI names real objects, builds a sentence about them |

## Level system

Level 1 is the default. Completing Sound Out, Word Builder, First Then, Trace It, and
Take Turns once each unlocks **Level 2** — harder words, letters instead of shapes, longer
routines, and a bigger matching board. Calm Corner and Photo Hunt sit outside the level
system on purpose.

Progress (stars, cleared activities, level) resets whenever the app is closed or reloaded.
This is intentional — every session starts fresh and pressure-free, with no streaks to
protect and no history to feel bad about.

## Design principles

- **No failure states.** Wrong answers are refused or gently reset, never marked wrong.
- **Predictability.** Every activity uses the same color throughout, and the Home button
  always sits in the same top-left spot.
- **Repetition is capped.** Repeating the same word/action is limited (usually to 3, or to
  a single use) so the app doesn't accidentally reinforce perseveration on a satisfying tap.
- **Session-based, not tracked.** No login, no persistent history, no data leaves the device.

## Tech

Plain HTML/CSS/JS — no build step, no framework. Web Speech API for the voice, Canvas API
for tracing, and TensorFlow.js + MobileNet (loaded from a CDN) for on-device object
recognition in Photo Hunt. Everything runs client-side; nothing is uploaded anywhere.

## Hosting

Served via GitHub Pages so the app runs over `https`, which the camera feature (Photo Hunt)
requires. The file is deployed as `index.html` at the repository root.

## Privacy

No accounts, no analytics, no tracking. Photo Hunt processes camera frames entirely on the
device using a locally-run model — nothing is uploaded, and no photo is ever saved to disk.
The only network activity is a one-time download of fonts and the recognition model on
first use; the app works offline after that.

## Status

Actively evolving personal project, built and refined through real use with two kids.
