# Hi, I'm Mikio Abe

CCNP ENCOR certified Network Engineer with expertise in **SASE, SD-WAN, and Zero Trust architectures**, built on a strong foundation of enterprise and service provider networking.

---

## 🛠 Technical Skills

**SASE / Zero Trust:** Cloudflare Zero Trust (SWG, ZTNA, WARP)
**SD-WAN:** FortiGate SD-WAN, IPsec/VRF integration
**Networking:** MPLS L3VPN, BGP, OSPF, EIGRP, VRF
**VPN Technologies:** IPsec, WireGuard, DMVPN, GRE
**Service Provider:** MPLS, BGP VPNv4, LDP
**Tools:** EVE-NG Pro, Wireshark, TCPDump, GNS3
**Certifications:** CCNP ENCOR | Fortinet NSE4 (In Progress)

---

## 🔬 Lab Overview

### SASE × SD-WAN Verification Lab

A comprehensive verification environment integrating MPLS underlay, SD-WAN overlay, and SASE security layers.

```
Site A                                             Site B
┌─────────┐                                   ┌─────────┐
│ SD-WAN  │                                   │ SD-WAN  │
│  Edge   │                                   │  Edge   │
└────┬────┘                                   └────┬────┘
     │                                             │
     │  ┌─────────────────────────────────────┐    │
     │  │         MPLS Core (VRF)             │    │
     ├──┤  CE ─── PE ═══════ PE ─── CE        ├────┤
     │  └─────────────────────────────────────┘    │
     │                                             │
     │  ┌─────────────────────────────────────┐    │
     └──┤      SASE Path (Internet)           ├────┘
        │ WireGuard ─── Gateway ─── WireGuard │
        └─────────────────────────────────────┘
```

**Architecture Layers:**
- **Underlay:** MPLS L3VPN (CE-PE-PE-CE)
- **Overlay:** SD-WAN with dual-path IPsec tunnels
- **Security:** SASE (SWG, ZTNA, DNS filtering)

---

## 🚀 Key Components

Each component demonstrates hands-on implementation with architectural documentation:

| Component | Description | Details |
|-----------|-------------|---------|
| **SASE / Zero Trust** | SWG, ZTNA, TLS Inspection, DNS Filtering | [View →](./SASE-ZeroTrust) |
| **SD-WAN** | Dual-path Design, Health Check, SLA-based Failover | [View →](./SD-WAN) |
| **Enterprise / SP** | MPLS L3VPN, BGP Policy, VRF Design | [View →](./Enterprise-SP) |
| **Brownout Detection** | Latency Injection, Quality Degradation, Path Switching | [View →](./Brownout) |
| **Troubleshooting** | Packet Capture, Visibility Boundaries, Encrypted Tunnel Analysis | [View →](./Troubleshooting) |

---

## 🎯 Current Focus

- Building SASE/SD-WAN lab environments for enterprise use cases
- Fortinet NSE4 certification
- Exploring VeloCloud on EVE-NG
- *(Optional: Zscaler ZDTA certification)*

---

## 📫 Contact

- **Location:** Tokyo, Japan
- **LinkedIn:** [Connect with me](#)

---

*Bridging traditional enterprise networking with modern SASE architectures*

