# Dante Routing Overview

This document outlines Dante RX channel assignments for the FOH M32 console and the livestream infrastructure as configured in February 2025.

---

## FOH M32 Dante RX
### Ref & Loop Tracks from Loop Mac Mini

| Track Name        | Channel |
|-------------------|---------|
| Click             | 1       |
| Cues              | 2       |
| Ref 3             | 3       |
| Ref 4             | 4       |
| Percussion        | 5       |
| Acoustic Guitar   | 6       |
| Electric Guitar   | 7       |
| Synth Bass        | 8       |
| Pads              | 9       |
| Keys              | 10      |
| Vocals            | 11      |
| Other             | 12      |
| Extra Tracks      | 13–16   |

### Computer Audio
- Spotify: Channels 1–2 (from ProPresenter Mac Mini)
- ProPresenter Audio: Channels 3–4

---

## Livestream Dante RX (Mac Mini)

### FOH M32 Sends (Live Band Channels)
| Source          | Dante Ch |
|-----------------|----------|
| Drums           | 1–8      |
| Bass            | 9        |
| Acoustic Guitar | 10       |
| Keys            | 11–12    |
| Electric Guitars| 13–16    |
| Vocals          | 17–22    |
| Spare / Comm    | 23–24    |

### Loop Tracks (Stereo)
| Instrument Group | Channels |
|------------------|----------|
| Percussion       | 17/18    |
| Acoustic Guitar  | 19/20    |
| Electric Guitar  | 21/22    |
| Synth Bass       | 23/24    |
| Pads             | 25/26    |
| Keys             | 27/28    |
| Vocals           | 29/30    |
| Other            | 31/32    |

---

## FOH Master to Auditorium Speakers

| Output | Channels |
|--------|----------|
| FOH Master (Stereo) | 31/32 |
| Speaker Input       | 1/2   |

All audio routing is synchronized over Dante with virtual soundcards enabled on each Mac, routed weekly in Dante Controller.
