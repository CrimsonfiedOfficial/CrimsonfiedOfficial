
<div align="center">

# Security Researcher · C++ 

**I break things on purpose so they can be fixed (or understood).**

Reverse engineering, protocol exploitation, and native tooling across **physical security**, **embedded devices**, and **game environments**.

[![Dahua Research](https://img.shields.io/badge/focus-Dahua_Research-red?style=for-the-badge)](https://github.com)
[![C++](https://img.shields.io/badge/C++-20-blue?style=for-the-badge&logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![Qt](https://img.shields.io/badge/Qt-6.7-41cd52?style=for-the-badge&logo=qt&logoColor=white)](https://www.qt.io/)
[![Python](https://img.shields.io/badge/Python-3%20tools-3776AD?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
</div>

---

## About

I work at the intersection of **offensive security research** and **systems programming**, taking apart black box protocols, mapping attack surfaces, and shipping real tools in **C++**, not just writeups.

My primary research lane is **Dahua Technology**: P2P cloud tunnels, digest auth, two-way audio paths, serial validation, firmware-era CVEs, and enterprise software like EIMS. I document what I find, build reproducible test harnesses, and write the kind of advisory material defenders actually need.

Outside surveillance gear, I spend time in **game security**, internals, injection surfaces, anticheat evasion. 

> Authorized testing and responsible disclosure only. Everything public is education, defense, or tooling.

---

## What I Do

<table>
<tr>
<td width="50%" valign="top">

### Dahua

- P2P protocol RE (`Easy4IP`, PTCP relay, WSSE auth)
- Unauthenticated & authenticated attack surface mapping
- Two-way talk / audio channel research
- CVE analysis & long-form advisory writing
- Enterprise targets (EIMS, VMS integrations)
- Serial pools, cloud validation, tunnel proxies

</td>
<td width="50%" valign="top">

### C++ & Native Tooling

- Qt6 / QML desktop apps with real SDK integration
- Multi-threaded network clients (`stop_token`, async I/O)
- Video pipelines, live view, playback, PTZ control
- CMake, MSVC, modern C++20 patterns
- Python probes for rapid protocol iteration

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Game Hacking / RE

- Process memory layout & module analysis
- Hooking, injection, and debugger-assisted RE
- Anti-cheat & integrity mechanism study
- Internal tooling and cheat-adjacent frameworks
- Kernel/user boundary research (where relevant)

</td>
<td width="50%" valign="top">

### General Security

- OS command injection & RCE chain analysis
- PKI / trust-store failures on embedded devices
- DoS via reachable assertions & parser crashes
- Nuclei-style detection logic & IoC writing
- Shodan / ZoomEye asset surface mapping

</td>
</tr>
</table>

---

## Featured Work

### DHView (not released yet) — Dahua Camera Management (C++ / Qt6)

A native desktop platform for managing Dahua cameras

```
Live view · P2P cloud connect · PTZ · Playback · Two-way audio
Digest auth · XML device import · Dashboard · SQLite backend
Tunnel TCP proxy · SDK integration · Connection workers
```

| Layer | Stack |
|---|---|
| UI | Qt 6.7, QML, Quick Controls 2 |
| Core | C++20, CMake, MSVC |
| Network | Custom P2P client, WSSE, relay/direct fallback |
| Media | SDK video sink, optional Qt Multimedia talk path |
| Data | SQLite repositories, device statistics |

---

### CVE Research & Advisories

Long form, defender oriented writeups, not NVD copypaste.

| CVE | Severity | Topic |
|---|---|---|
| **CVE-2024-13985** | `10.0` CRITICAL | EIMS `capture_handle.action` unauthenticated RCE |
| **CVE-2026-29116** | `8.7` HIGH | Unauthenticated remote DoS (multi-product) |
| **CVE-2026-29115** | `6.9` MEDIUM | Authenticated remote DoS (IPC / SD) |
| **CVE-2026-29114** | `2.3` LOW | Exposed device CA root / trust-chain abuse |

Each advisory includes CVSS 4.0 breakdowns, CWE analysis, exploitation context, detection guidance, and remediation — the full picture.

---

### Research Tooling

| Tool | Purpose |
|---|---|
| `test_p2p_handshake.py` | Full Easy4IP UDP handshake — mirrors production P2P flow |
| `test_full_p2p.py` / `p2p_connect_test.cpp` | End-to-end tunnel validation in Python & C++ |
| `test_relay_connect.py` | Relay path probing |
| `test_serial_cloud.py` | Cloud serial validation |
| `export_talk_serials.py` | Talk-channel serial enumeration & pooling |
| `TunnelTcpProxy` | Local TCP bridge through P2P tunnel |

Protocol research starts in Python. Production code lands in C++.

---

## Tech Stack

```text
Languages     C++20 · Python 3 · QML · SQL
Frameworks    Qt 6 · CMake · Google Test
Platforms     Windows (primary) · Linux-adjacent tooling
Security      Wireshark · custom probes · nuclei templates · CVE/NVD/CNVD
RE / Debug    x64dbg · IDA-class workflows · memory editors · driver theory
Build         MSVC 2019 · Ninja · Qt Maintenance Tool
```

---
## How I Think

```text
1. goon

2. Read the source, protocol, and data formats before trusting the abstraction layer

3. If something connects to the internet, assume the edge cases matter

4. A library isn't truly understood until I can recreate the important parts myself

5. Games, cameras, servers, and apps all have the same weakness:
   input goes in, assumptions come out

6. Debugging is just reverse engineering with better lighting

7. Document what I learn so others can build on it

8. Music, code, and security are all the same process:
   understand the structure, then create something new
```
---

## Current Focus

- [ ] Expanding **DHView** — smarter P2P validation, talk path hardening, fleet dashboards
- [ ] Mapping **Dahua 2026 PSI** disclosure batch across IPC/NVR/EIMS estates
- [ ] Correlating **serial-prefix pools** with exploitable talk firmware branches
- [ ] Native **C++** performance passes on tunnel and video hot paths
- [ ] Game security — internal RE tooling and anti-cheat surface documentation

---

## Connect

Telegram: @nicotine_feind

| | |
|---|---|
| **GitHub** | [@CrimsonfiedOfficial](https://github.com/CrimsonfiedOfficial) |
| **Research** | Dahua P2P · CVE advisories · native tooling |
| **DMs** | Open for collab on RE, CVE validation, or C++ architecture - not for illegal access |

---


</div>
