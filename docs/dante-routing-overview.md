# Dante Routing Overview

This file outlines how audio is routed across our Dante network, including channel assignments for the FOH M32 console and the Livestream system as of February 2025.

Everything here was made possible through the collaboration of our volunteer IT and Audio teams, and gets tweaked as our needs evolve.

---

## FOH Console (M32) — Dante Inputs

These channels come into the M32 via Dante from two primary computers: the **Ableton Loop Mac** and the **ProPresenter Mac**.

### Loop Mac (Ableton Live - Clicks, Cues, Stems)

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

### ProPresenter Mac Mini (General Playback)

- **Spotify**: Channels 1–2  
- **ProPresenter Audio**: Channels 3–4

---

## Livestream Mac Mini — Dante RX

This computer receives its audio from the FOH M32 and the Loop Mac. It mixes everything in Ableton Live and sends it to our Resi streaming system.

### FOH M32 Sends (Live Band)

| Source            | Channels |
|-------------------|----------|
| Drums             | 1–8      |
| Bass              | 9        |
| Acoustic Guitar   | 10       |
| Keys              | 11–12    |
| Electric Guitars  | 13–16    |
| Vocals            | 17–22    |
| Spare / Comms     | 23–24    |

### Loop Tracks (Stereo Redundant Feed)

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

## FOH Output to Speakers

The M32 sends its main stereo output over Dante to a 2-channel AVIO adapter that feeds our main speaker DSP.

| Output            | Channels |
|-------------------|----------|
| FOH Master Bus    | 31/32    |
| Speaker Input     | 1/2      |

---

## Final Notes

- All Macs run **Dante Virtual Soundcard**
- Channel mappings are managed in **Dante Controller**, adjusted weekly
- The **M32 acts as Dante clock master**
- Static IPs and VLAN isolation keep traffic stable and separate from general use

This setup lets us keep everything in sync — audio, lighting cues, and video playback — while making the system easier for volunteers to operate and adapt.
