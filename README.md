# Dante AV Infrastructure Deployment — From Analog to IP

## Project Summary

This project documents our church’s move from a completely analog audio setup to a modern Dante-based IP network. Before 2022, we didn’t have digital routing, remote access, or any scalable way to manage FOH, livestream, or playback systems.

I led the shift as Worship Arts Pastor, but I was supported every step of the way by our volunteer IT and Audio teams. The result was a full rebuild that brought our system into the digital age — with room to grow.

We now run FOH, livestream, Ableton playback, lighting, and stage monitoring across a VLAN-isolated Dante network with centralized control.

## My Role

I served as the project lead — planning, budgeting, and coordinating implementation. I leaned heavily on our IT and audio volunteers for key pieces like switch configuration, cabling, and VLAN setup.

My part in this included:

- Proposing the upgrade and presenting to leadership
- Drafting the full $50,000 CAD budget (and staying under it)
- Coordinating IP assignments, static routes, and VLANs with our IT team
- Selecting gear, managing vendors, and receiving equipment
- Designing Dante + AES50 routing to fit our multi-room workflow
- Running cable (SDI, Cat5e, DMX, Cat6 shielded, XLR) across the building
- Enabling remote support via TeamViewer with MFA

I also wrote out documentation so the team could understand and support the system going forward.

## Why We Chose Dante

Dante wasn’t an obvious choice at first — a lot of us were used to analog boards and patch panels. But the need to separate livestream audio and FOH, along with the flexibility to route audio between rooms, led us to commit to it.

We chose Dante because it allowed us to:

- Keep FOH, livestream, and stage IEM mixes independent
- Send audio/midi/stems between rooms with zero signal loss
- Use Dante Controller to adapt routing in real time
- Add lighting/MIDI support over IP in the future
- Train volunteers with consistent and predictable workflows

## System Overview

- **Midas M32** FOH console (Dante card installed – master clock)
- **Behringer X32 Rack** (for IEMs — connected via AES50)
- **Two DL16** stage boxes (AES50 daisy-chained)
- **Mac Minis**:
  - Livestream: Receives audio + pushes to Resi/YouTube
  - Ableton: Multitracks, cues, stems
  - ProPresenter: Slides, video, and Spotify
  - LightKey: Lighting control
- **Dante VLAN** with static IPs + managed switches
- **Dante Controller** for signal routing + sync
- **Remote access** via TeamViewer (with MFA) for FOH and Livestream computers

## Budget and Procurement

I managed the full purchasing and vendor workflow using spreadsheets and leadership review. We reused what we could and upgraded what was needed for long-term reliability.

- **Approved Budget**: $50,000 CAD  
- **Actual Spend**: $45,525.96 CAD  
- **Savings**: ~$4,474 CAD

## Weekly Ops

Each week I support Sunday operations by:

- Adjusting Dante routing for FOH/livestream
- Updating Ableton channel outputs for multitrack sessions
- Troubleshooting sync and routing issues
- Helping volunteers rotate through the AV/Livestream stations (7 operators per week)

## Cloud/Security Relevance

This wasn’t a cloud project, but it mirrors a lot of cloud principles:

- **VLANs, subnets, and static IPs** are like designing secure VPCs
- **Dante Controller** acts like a real-time control plane
- **TeamViewer MFA** is similar to jump-host or bastion access
- **Ongoing routing changes and logging** reflect change control + uptime

The experience here — designing secure, scalable infrastructure with weekly ops — aligns well with cloud security architecture work.

## Documentation

- `docs/setup.md`: Full install + routing setup
- `docs/ableton-routing-map.md`: How return tracks map to Dante channels
- `docs/dante-routing-overview.md`: System-wide Dante signal flow
- `docs/failover-remote-access.md`: Remote control plans + recovery notes
- `docs/budget-summary.md`: Full itemized cost breakdown
- `images/docs/legacy/README.md`: Original brainstorm drawings and sketches

## Final Thoughts

While I don’t pretend to be a network engineer, this project taught me a lot — not just about Dante and VLANs, but also how to lead a team and build systems that others can use and support.

I’m proud of what we built together. It’s reliable, flexible, and future-ready — thanks to collaboration, planning, and a great volunteer team.

**Project Lead**: Ryan Gillies (Worship Arts Pastor)  
**Collaborators**: Volunteer Audio + IT Team

---

### Security & Privacy Notice

This repo avoids exposing any sensitive info — no IP addresses, MAC addresses, or login credentials are shared here. Procurement docs with serials, vendor info, and invoices are stored privately. All remote access is MFA-protected.

This documentation exists to show the architecture, teamwork, and planning behind the system — not to expose private infrastructure.

