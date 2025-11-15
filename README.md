# Wireshark Network Traffic Analysis

**Author:** Ankit Jaiswal

## Overview
This project captures and analyzes network traffic from a personal lab network using **Wireshark**. The goal is to inspect and document common protocol behaviors (DNS, HTTP, ARP) and learn basic packet-analysis techniques used in network troubleshooting and cybersecurity.

## Files in this repository
- `report.pdf` — one-page summary of findings (PDF for upload)
- `filters.txt` — useful Wireshark display filters used in the analysis
- `screenshots/` — screenshots: DNS query, HTTP stream, ARP request/reply
- `capture.pcapng` (optional) — raw packet capture file (if included)

## Steps performed
1. Installed Wireshark with Npcap (admin-only, 802.11 monitor mode, WinPcap compat enabled).
2. Captured packets on the active interface for ~2 minutes while generating DNS, HTTP, and ARP traffic.
3. Applied display filters (`dns`, `http`, `arp`) and inspected packet details.
4. Saved screenshots and documented key observations in `report.pdf`.

## Key findings (summary)
- DNS: Observed standard DNS queries and responses; domain `example.com` resolved to 93.184.216.34.
- HTTP: Observed an HTTP GET request and 200 OK response from local test server; headers visible in HTTP stream.
- ARP: Observed ARP request and reply showing mapping of IP to MAC address on the LAN.

## How to reproduce
1. Install Wireshark and Npcap (select admin-only, 802.11 monitor mode, WinPcap compat).
2. Run Wireshark → select interface → Start capture.
3. Generate traffic (visit a site / ping router / run local HTTP server).
4. Stop capture → apply display filters → export screenshots.
