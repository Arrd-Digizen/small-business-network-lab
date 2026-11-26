# IP Addressing Plan — SINGLE SOURCE OF TRUTH

**Law of this lab:** every IP, VLAN ID, and device name below is fixed.
If anything must change, this file is updated FIRST, then the devices.
Never improvise values mid-build.

## Status: Phase 0 — nothing configured yet

## Phase 1 — flat LAN (planned)
| Device | IP | Notes |
|---|---|---|
| PC1 | 192.168.1.10/24 | static |
| PC2 | 192.168.1.11/24 | static |
| Network | 192.168.1.0/24 | no gateway needed yet |

## Phase 2 — second LAN (planned)
| Device | IP | Notes |
|---|---|---|
| R1 G0/0 (LAN 1) | 192.168.1.1/24 | becomes PC1/PC2 default gateway |
| R1 G0/1 (LAN 2) | 192.168.2.1/24 | becomes LAN 2 default gateway |
| Network 2 | 192.168.2.0/24 | |

## Phase 3+ — VLANs (planned)
| Item | Value | Notes |
|---|---|---|
| VLAN 10 STAFF | 192.168.10.0/24 | gateway 192.168.10.1 (R1 subinterface) |
| VLAN 20 SERVERS | 192.168.20.0/24 | gateway 192.168.20.1 (R1 subinterface) |
| VLAN 30 GUEST | 192.168.30.0/24 | gateway 192.168.30.1 (R1 subinterface) |
| SW1 management SVI | 192.168.10.2/24 | on VLAN 10 |
| SW2 management SVI | 192.168.10.3/24 | on VLAN 10 |
| SRV1 | 192.168.20.10/24 | static |
| DHCP pools | .100–.199 per VLAN | each pool excludes everything below .100 and above .199 |

## Phase 6 — WAN stretch (planned, only if I choose it)
| Item | Value | Notes |
|---|---|---|
| WAN link | 203.0.113.0/30 | R1 = 203.0.113.2, ISP = 203.0.113.1 |
| Fake internet server | 198.51.100.10 | simulated public host |

## Naming law
- Hostnames always equal device names (R1, SW1, SW2, PC1...).
- Domain: `lab.local`; SRV1 serves DNS + HTTP for `intranet.lab.local`.
- Simulation-only login: user `admin`, password `Lab@123` — documented as lab credentials only.