# Failover & Remote Access Strategy

## Purpose

When something breaks during a live event, quick access can make the difference between a small hiccup and a major disruption. Remote access allows trusted team members to troubleshoot audio, slides, or routing without needing to be on-site.

## Setup Overview

- **TeamViewer** is installed on:
  - FOH iMac (Sound Room)
  - Livestream Mac Mini (Ableton + Resi mix)
- **Multi-factor authentication (MFA)** is enabled
- Both machines are part of a **dedicated AV VLAN**
- **Dante Controller** is installed on both for remote routing adjustments
- Typical uses include:
  - Fixing Dante signal routing in real time
  - Restarting Dante Virtual Soundcard or Ableton Live
  - Unfreezing MIDI or slide triggering issues
  - Helping volunteers through routing or playback issues mid-service

## Access & Permissions

- Access is limited to the **Project Lead** (Ryan Gillies) and approved volunteers from the **IT and Audio team**
- Device IPs are **reserved by MAC address** on the network switch/router
- Remote access is **not exposed to public or general-use networks**

## Notes

Having remote access to our Dante network has helped us quickly resolve issues without disrupting the flow of live operations. While it’s not a full-scale IT recovery system, this lightweight approach has proven reliable, safe, and team-friendly.


