<!-- Copy this file to your GitHub profile repo: github.com/<username>/<username>/README.md -->

<div align="center">

# Security Researcher · C++ · Low-Level Systems

**I break things on purpose so they can be fixed (or understood).**

Reverse engineering, protocol exploitation, and native tooling across **physical security**, **embedded devices**, and **game environments**.

[![Dahua Research](https://img.shields.io/badge/focus-Dahua_Research-red?style=for-the-badge)](https://github.com)
[![C++](https://img.shields.io/badge/C++-20-blue?style=for-the-badge&logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![Qt](https://img.shields.io/badge/Qt-6.7-41cd52?style=for-the-badge&logo=qt&logoColor=white)](https://www.qt.io/)
[![Python](https://img.shields.io/badge/Python-3%20tools-3776AD?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
</div>

---

## About

I work at the intersection of **offensive security research** and **systems programming** — taking apart black-box protocols, mapping attack surfaces, and shipping real tools in **C++**, not just writeups.

My primary research lane is **Dahua Technology**: P2P cloud tunnels, digest auth, two-way audio paths, serial validation, firmware-era CVEs, and enterprise software like EIMS. I document what I find, build reproducible test harnesses, and write the kind of advisory material defenders actually need.

Outside surveillance gear, I spend time in **game security** — memory internals, injection surfaces, anti-cheat evasion theory, and the kind of low-level Windows/Linux work that translates directly between domains. Same skills, different binaries.

> Authorized testing and responsible disclosure only. Everything public is education, defense, or tooling.

---

## What I Do

<table>
<tr>
<td width="50%" valign="top">

### Dahua / Physical Security

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

### [DHView](https://github.com) — Dahua Camera Management (C++ / Qt6)

A native desktop platform for managing Dahua estates — not a wrapper around someone else's VMS.

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

Built because understanding a protocol means **implementing it**, not screenshotting someone else's tool.

---

### CVE Research & Advisories

Long-form, defender-oriented writeups — not NVD copy-paste.

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
1. Read the wire format before reading the blog post
2. If the vendor says "XSS" but CVSS says availability-only — trust the math
3. Unauthenticated beats authenticated; RCE beats reboot; reboot still matters
4. A protocol isn't understood until your client connects without their SDK
5. Game AC and camera firmware both lie about how much they validate input
6. Document for the blue team, build for yourself
```

---

## Current Focus

- [ ] Expanding **DHView** — smarter P2P validation, talk path hardening, fleet dashboards
- [ ] Mapping **Dahua 2026 PSI** disclosure batch across IPC/NVR/EIMS estates
- [ ] Correlating **serial-prefix pools** with exploitable talk firmware branches
- [ ] Native **C++** performance passes on tunnel and video hot paths
- [ ] Game security — internal RE tooling and anti-cheat surface documentation

---

## Stats


![GitHub Stats](https://github-stats-extended.vercel.app/api?username=crimsonfiedofficial&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&title_color=ff4444&icon_color=ff4444)

![Top Languages](https://github-stats-extended.vercel.app/api/top-langs/?username=crimsonfiedofficial&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&langs_count=8)

---

## Connect

Telegram: @nicotine_feind

| | |
|---|---|
| **GitHub** | [@CrimsonfiedOfficial(https://github.com/CrimsonfiedOfficial) |
| **Research** | Dahua P2P · CVE advisories · native tooling |
| **DMs** | Open for collab on RE, CVE validation, or C++ architecture - not for illegal access |

---

<div align="center">

```cpp
// typical Tuesday
auto tunnel = P2PClient::connectCamera(serial);
if (!tunnel) return exploit_surface_not_exhausted_yet;
// ...understand the box, then decide what to report
```

</div>
