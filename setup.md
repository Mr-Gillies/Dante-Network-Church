# System Setup & Routing Overview

## 1. Dante & AES50 Routing — How We Connected Everything

This setup outlines how our Dante audio network and AES50 stage connections were wired and routed. This was a learning experience for me and our team — and I’m thankful for the volunteer IT and Audio support that helped make it possible.

The **Midas M32 console** acts as the heart of the system, providing both the **master clock for Dante** and the main routing hub for all audio signals.

---

## Stage and Monitoring Design

- Two DL16 stage boxes were installed on either side of the stage and **daisy-chained via AES50**.
- Those connect directly to the **M32**, which serves as our FOH console.
- The M32 also feeds signals to our **X32 Rack**, which handles **in-ear monitor mixing** for the band.
- The X32 then returns those mixes back out to the DL16s, which feed the **IEM transmitters**.

This keeps our FOH mix and monitor mix separate — a big win in terms of clarity and volunteer workflow. It also keeps the stage cabling minimal and easy to manage.

---

## Dante Network Summary

We set up a dedicated Dante network that runs independently from our regular church IT systems. That included:

- **Static IPs** on a private Dante subnet
- **Dedicated VLAN** just for Dante traffic
- **Managed gigabit switch**
- **M32** as the Dante clock master
- **Dante Controller** to manage audio routing

---

### Dante Inputs (to M32)

- **ProPresenter Mac Mini**  
  - Ch 1–2: Spotify  
  - Ch 3–4: Video/audio playback

- **Ableton Loop Mac Mini**  
  - Ch 1: Click  
  - Ch 2: Cues  
  - Ch 3–4: Reference  
  - Ch 5–12: Multitracks (e.g., drums, bass, keys, etc.)  
  - Ch 13–16: Extra vocals or stems  
  - Ch 21–32: Reserved for special songs/setups

---

### Dante Outputs (from M32)

- Ch 1–24: FOH instrument groups (drums, AG, EG, vocals, etc.)
- Ch 17–32: Ableton stems (sent to Livestream)
- Ch 1–4: ProPresenter/Spotify (mirrored as needed)
- Ch 45–48: Overflow channels, future use

---

### FOH Speaker Output

- The M32 stereo master mix is routed to Dante Ch 31–32.
- We use a **Dante AVIO XLR adapter** to convert that digital signal to analog for our speaker processor.

---

## Why We Went This Route

Before this, we were running an entirely analog setup. Patch cables, shared mixes, and no way to expand without more wiring. It worked, but it was limiting.

We chose Dante because it gave us:

- Clean separation between FOH and livestream audio
- Digital routing (no more crawling under desks to rewire)
- Reduced analog noise and better signal quality
- Remote monitoring and backup access
- Future-proofing for lighting, MIDI, and more

We’re still learning, but this system has made our weekly services smoother and more flexible — especially with volunteers rotating through different stations.

---

## Notes on Networking

Each Dante computer runs **Dante Virtual Soundcard**, and everything is kept in sync with the M32 as the primary clock. All devices use static IPs, and routing is handled using **Dante Controller** each week based on the current service layout.

---

This isn’t a perfect system — but it’s been a solid one. It helped us move from a patch-heavy analog world into something that’s digital, reliable, and scalable for the future. Grateful to have had help from our volunteer team every step of the way.
