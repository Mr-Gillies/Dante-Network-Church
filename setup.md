## 3. Dante & AES50 Routing Architecture (Network-Focused)

The Midas M32 acted as the **core of the system** — both the Dante master clock and the hub for signal routing. All audio sources and destinations passed through the M32, making it the central point for both **Dante-based digital audio** and **AES50 analog-stage routing**.

---

### Stage & Monitor Design

- Two DL16 stage boxes were **daisy-chained via AES50** and connected directly to the **M32 console**.
- These boxes were placed **stage left and stage right**, giving us physical XLR I/O on both sides of the platform.
- From the M32, signals were passed **via AES50 to the X32 Rack**, which handled **in-ear monitor mixes** independently of FOH.
- The **X32 sent monitor outputs back** through the AES50 chain to the DL16 outputs, which were hardwired to our **IEM transmitter rack**.

This layout resolved long-standing FOH vs. IEM balance issues by **separating the monitor mix architecture from the main house mix**, while keeping stage wiring clean and scalable.

---

### Dante Routing Summary

The Dante network was built on:

- **Static IPs** in a private subnet (e.g., 192.168.5.x)
- **Dedicated VLAN** for Dante traffic, isolated from general IT traffic
- **Managed 1 Gbps switch** used for all Dante-connected endpoints
- **M32** as the Dante sync master and primary TX/RX endpoint
- **Dante Controller** used to manage routing maps weekly

#### Inputs to M32 (via Dante RX)

- **ProPresenter Mac Mini**
  - Channels 1–2: Spotify
  - Channels 3–4: ProPresenter Audio

- **Ableton (Loop) Mac Mini**
  - Channel 1: Click
  - Channel 2: Cues
  - Channels 3–4: Reference audio
  - Channels 5–12: Multitracks (Percussion, Drums, Bass, Keys, etc.)
  - Channels 13–16: BGVs or extra stems
  - Channels 21–32: Reserved/flexible stems for special arrangements

#### Outputs from M32 to Livestream Mac (via Dante TX)

- Channels 1–24: FOH stem groups (e.g., drums, bass, AG, EG, keys, vocals)
- Channels 17–32: Direct stereo loop sends (mirrored from Ableton)
- Channels 1–4: ProPresenter/Spotify (redundant)
- Channels 45–48: Reserved for overflow, special routes, or future use

#### Output to FOH System

- M32 master stereo bus routed to Channels 31–32
- Received by the DSP or speaker processor directly via Dante

---

### Network & Routing Design Intent

Before this upgrade, our system was entirely **analog, patch-based, and limited** in flexibility. There was no reliable way to isolate different mixes or add flexibility without significant rewiring.

As project lead, I moved us toward Dante because:

- It allowed **separation of FOH and livestream mixes**
- We could assign and reassign routing digitally without physical patching
- It reduced analog noise and interference
- It enabled **remote monitoring and failover support**
- It offered long-term scalability for additional endpoints (e.g., lighting, automation)

All Dante endpoints — including the M32 and all Mac Minis — were configured with static IPs and properly clocked via the M32. Each computer used **Dante Virtual Soundcard**, and routing was fully managed through Dante Controller.

---

This setup gave us a clean, scalable, and reliable infrastructure — replacing patch chaos with centralized, network-based audio that’s maintained weekly and built for growth.
