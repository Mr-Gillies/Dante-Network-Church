# Dante AV Infrastructure Deployment — From Analog to IP

## Project Summary

This project documents the full rebuild of our church’s audio infrastructure. Before 2022, we were entirely analog — no digital routing, no Dante, and no network scalability. As Worship Arts Pastor, I led the shift to a Dante-based IP audio network that now supports FOH, livestream, stage monitoring, and digital audio playback.

The final system includes four dedicated Mac Minis running Ableton Live, ProPresenter, LightKey, and Dante Virtual Soundcard — all synchronized over a VLAN-isolated Dante network with centralized control.

## My Role

I served as project lead with full authority over direction, budgeting, purchasing, and technical deployment. My responsibilities included:

- Building a line-item budget with links, costs, and justifications
- Presenting to leadership and securing a $50,000 CAD budget
- Directing the IT team on static IPs, subnet design, and VLAN segmentation
- Selecting gear, overseeing procurement, and managing vendor logistics
- Designing the routing and network flow using Dante Controller and AES50
- Installing cabling (Cat6, SDI) across facilities including attic work
- Setting up failover and remote access support for live operations
- Maintaining weekly Dante routing and Ableton integration

This project modernized our entire workflow — from analog and patch bays to digital IP audio, fully documented and team-ready.

## Why We Chose Dante

In 2022, there was hesitation around using Dante. It was unfamiliar, and most of our volunteers were used to analog methods. I made the call to move forward based on:

- The need to separate FOH and livestream mixes
- Flexible routing of tracks and stems between multiple systems
- Reducing signal degradation and analog grounding noise
- Remote access and diagnostics through a centralized controller
- Future scalability (lighting, MIDI, livestream sync)

Dante offered the best long-term path for reliable, scalable audio infrastructure.

## System Overview

- **Midas M32** FOH console with Dante expansion card (master clock & sync)
- **Behringer X32 Rack** monitor console via AES50
- **Two DL16** stage boxes (daisy-chained via AES50 for stage I/O)
- **Four Mac Minis**:
  - Ableton playback (clicks, cues, stems)
  - Livestream (Ableton Live mixing)
  - ProPresenter (media + Spotify)
  - LightKey (stage lighting)
- **All Macs connected via Dante VLAN** with static IPs and managed switch
- **Dante Controller** for signal flow configuration and monitoring
- **TeamViewer with MFA** installed on all Macs for secure remote control

The M32 handled all Dante routing to and from stage, playback, and broadcast systems.

## Budget and Procurement

I created and managed the entire procurement workflow using a detailed spreadsheet with URLs, categories, and cost tracking. I worked closely with church leadership to control costs while building for future expansion.

- **Approved Budget**: $50,000 CAD  
- **Final Spend**: $45,525.96 CAD  
- **Savings**: ~$4,474

We reused gear where possible and prioritized long-term durability over short-term convenience.

## Weekly Responsibilities

Each week, I continue to oversee system function and readiness:

- Manage Dante routing for FOH, livestream, and IEMs
- Confirm sync and signal flow between Macs and consoles
- Reassign Ableton output channels for updated setlists
- Support the team with training, troubleshooting, and routing adjustments

## Cloud/Security Relevance

While this wasn’t a traditional cloud project, the parallels are strong:

- **VLANs & IP Planning** mirror cloud VPC/subnet design
- **Static routing** is similar to managing service endpoints
- **TeamViewer with MFA** parallels bastion access/gateway control
- **Dante Controller** is effectively a real-time control plane
- **Weekly ops and incident handling** reflect uptime SLAs and change management

This project required secure architecture, documentation, and hands-on ops — skills that translate directly into cloud and security roles.

## Documentation

- `docs/setup.md`: Full install and routing guide
- `docs/ableton-routing-map.md`: Return track sends → Dante channels
- `docs/dante-routing-overview.md`: Input/output routing across devices
- `docs/failover-remote-access.md`: Remote control and recovery plan
- `docs/budget-summary.md`: Final cost categories and budget notes

## Final Thoughts

This was a ground-up infrastructure upgrade with real operational weight. I was fully responsible for the outcome — from the attic wiring to the last Ableton channel. What we built is reliable, maintainable, and modern.

**Project Lead**: Worship Arts Pastor

---

### Security & Privacy Notice

This public repo omits full budget line items, serial numbers, and internal access credentials in order to protect sensitive organizational data. Detailed procurement tracking was done internally and included vendor links, pricing, and invoicing.

As someone pursuing cloud security, I take care not to expose confidential or infrastructure-specific information unnecessarily. This documentation highlights the architecture and leadership behind the project — not privileged or sensitive data.
