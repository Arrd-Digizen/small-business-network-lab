# Small-Business Network Lab — Cisco Packet Tracer

A small-business network that I design, build, break, and fix from scratch in
Cisco Packet Tracer, one phase at a time — while learning networking on the job
as an IT support technician aiming for a junior network/sysadmin role.

> **Honesty note:** everything in this repo is a self-built **simulation learning
> lab**. It documents my learning process, not production experience.

## Status
See [PROGRESS.md](PROGRESS.md) for exactly where the build stands right now.

## Tools
| Tool | Version |
|---|---|
| Cisco Packet Tracer | 9.0.0 (verified via Help → About in my installation) |
| Host OS | Windows |

## Devices (model names verified in my PT installation)
| Role | Device in PT |
|---|---|
| R1 — gateway router | Cisco 1941 |
| SW1, SW2 — access switches | Cisco 2960 |
| PC1–PC3 — staff/guest clients | PC-PT |
| SRV1 — internal server (DNS + HTTP) | Server-PT |

## Build roadmap
| Phase | Build | Status |
|---|---|---|
| 0 | Install/verify PT, repo + skeleton | in progress |
| 1 | Flat LAN: 1 switch, 2 PCs, static IPs, first pings | planned |
| 2 | Two LANs + R1 routing between subnets | planned |
| 3 | VLANs 10/20/30, trunks, router-on-a-stick | planned |
| 4 | DHCP per VLAN + DNS/HTTP server | planned |
| 5 | ACLs, SSH only, port security | planned |
| 6 | Stretch: ISP edge, NAT/PAT, fake internet | stretch |
| 7 | Diagrams, config exports, interview prep | planned |

## Repo map
- `README.md` — you are here
- `PROGRESS.md` — live build state (done, next, open issues)
- `future-improvements.md` — good ideas parked out of scope
- `docs/` — one doc per phase + addressing plan + troubleshooting log
- `verification/` — my actual screenshots as proof
- `packet-tracer/` — .pkt lab files (appears with Phase 1)
- `configs/` — device config exports (appear from Phase 2)
- `diagrams/` — topology diagrams (appear in Phase 7)

## How this is built
Each phase has its own doc in `docs/` with the commands used (each with a one-line
"why"), verification screenshots from my own runs, problems I actually hit, and
interview-style Q&A. `docs/ip-addressing-plan.md` is the single source of truth
for every IP, VLAN, and name in the lab.