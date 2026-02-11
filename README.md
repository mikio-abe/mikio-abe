# Hi, I'm Mikio Abe

CCNP ENCOR certified Network Engineer with expertise in **SASE, SD-WAN, and Zero Trust architectures**, built on a strong foundation of enterprise and service provider networking.

**【日本語サマリ】**

CCNP ENCOR取得済みのネットワークエンジニア。SASE、SD-WAN、ゼロトラストアーキテクチャを専門とし、エンタープライズおよびサービスプロバイダーネットワークの経験を基盤としています。

---

## 🛠 Technical Skills

| Category | Skills |
|----------|--------|
| SASE / Zero Trust | Cloudflare Zero Trust (SWG, ZTNA, WARP) |
| SD-WAN | FortiGate SD-WAN, Cisco Viptela (vBond/vSmart/vEdge), IPsec/VRF integration |
| Networking | MPLS L3VPN, BGP, OSPF, EIGRP, VRF |
| VPN Technologies | IPsec, WireGuard, DMVPN, GRE |
| Service Provider | MPLS, BGP VPNv4, LDP |
| Tools | EVE-NG Pro, Wireshark, TCPDump, GNS3 |
| Certifications | CCNP ENCOR, CCNA, Linuc Level 1, Fortinet NSE4 (Preparing) |

**【日本語サマリ】**

Cloudflare Zero Trust、FortiGate SD-WAN、Cisco Viptela SD-WAN、MPLS L3VPN、各種VPN技術（IPsec、WireGuard、DMVPN）を習得。EVE-NG Pro等のラボ環境で検証実施。CCNP ENCOR、CCNA、Linuc Level 1取得済み、Fortinet NSE4準備中。

---

## 🚀 Key Components

Each component demonstrates hands-on implementation with architectural documentation:

| Component | Description | Details |
|-----------|-------------|---------|
| **SASE / Zero Trust** | SWG, ZTNA, TLS Inspection, DNS Filtering | [View →](https://github.com/mikio-abe/SASE-ZeroTrust) |
| **SD-WAN (FortiGate)** | Dual-path Design, Health Check, SLA-based Failover | [View →](https://github.com/mikio-abe/SD-WAN) |
| **SD-WAN (Cisco Viptela)** | CLI-only controller-based SD-WAN, Enterprise Root CA, OMP/BFD | [View →](https://github.com/mikio-abe/Cisco-Viptela-SD-WAN-CLI-Only-No-vManage-) |
| **Enterprise / SP** | MPLS L3VPN, BGP Policy, VRF Design | [View →](https://github.com/mikio-abe/Enterprise-SP) |
| **Troubleshooting** | Encrypted Tunnel Analysis, Visibility Boundaries | [View →](https://github.com/mikio-abe/Troubleshooting) |
| **Lab vs Production** | Differences between lab and production deployments | [View →](https://github.com/mikio-abe/Lab-vs-Production) |

**【日本語サマリ】**

各コンポーネントはハンズオン実装とアーキテクチャドキュメントで構成。SASE/Zero Trust、SD-WAN（FortiGate/Cisco Viptela）、Enterprise/SP（MPLS）、Troubleshooting、Lab vs Productionの6つのリポジトリで詳細を公開。

---

## 🔬 Lab Overview

### SASE × SD-WAN Verification Lab

A comprehensive verification environment integrating MPLS underlay, SD-WAN overlay, and SASE security layers.<BR>

<img width="750" alt="image" src="https://github.com/user-attachments/assets/0aec4f12-d0c4-493c-b884-d953714d0908" />

---
### AS Numbers

| Device | AS Number | Role |
|--------|-----------|------|
| CE1 | 65000 | Customer Edge (Site 1) |
| CE2 | 65000 | Customer Edge (Site 2) |
| PE1 | 65001 | Provider Edge (MPLS Core) |
| PE2 | 65001 | Provider Edge (MPLS Core) |
| FG1 | 65100 | FortiGate SD-WAN (Site 1) |
| FG2 | 65200 | FortiGate SD-WAN (Site 2) |
| CF-POP1 | 65300 | Cloudflare POP (Site 1) |
| CF-POP2 | 65400 | Cloudflare POP (Site 2) |

### Interface IP Addresses

#### MPLS Underlay

| Link | Device | Interface | IP Address | Subnet |
|------|--------|-----------|------------|--------|
| FG1 – CE1 | FG1 | port1 | 10.1.1.2 | /30 |
| | CE1 | e0/1 | 10.1.1.1 | /30 |
| CE1 – PE1 | CE1 | e0/0 | 10.101.1.2 | /30 |
| | PE1 | e0/0 | 10.101.1.1 | /30 |
| PE1 – PE2 | PE1 | e0/1 | 10.200.1.1 | /30 |
| | PE2 | e0/1 | 10.200.1.2 | /30 |
| PE2 – CE2 | PE2 | e0/0 | 10.102.1.1 | /30 |
| | CE2 | e0/0 | 10.102.1.2 | /30 |
| CE2 – FG2 | CE2 | e0/1 | 10.200.2.1 | /30 |
| | FG2 | port1 | 10.200.2.2 | /30 |

#### SASE Overlay

| Link | Device | Interface | IP Address | Subnet |
|------|--------|-----------|------------|--------|
| FG1 – POP1 | FG1 | port2 | 10.0.0.1 | /24 |
| | CF-POP1 | ens3 | 10.0.0.2 | /24 |
| FG2 – POP2 | FG2 | port2 | 10.0.1.1 | /24 |
| | CF-POP2 | ens3 | 10.0.1.2 | /24 |
| POP1 – POP2 | CF-POP1 | ens5 | Internet (fixed broadband) | — |
| | CF-POP2 | ens5 | Internet (mobile tethering) | — |

#### LAN

| Site | Device | Interface | IP Address | Subnet |
|------|--------|-----------|------------|--------|
| Site 1 | FG1 | port4 | 192.168.134.1 | /24 |
| Site 2 | FG2 | port3 | 192.168.20.1 | /24 |

#### Loopback

| Device | Interface | IP Address |
|--------|-----------|------------|
| PE1 | Loopback0 | 1.1.1.1 /32 |
| PE2 | Loopback0 | 2.2.2.2 /32 |
| CE1 | Loopback0 | 192.168.1.1 /24 |
| CE2 | Loopback0 | 192.168.2.1 /24 |

### Tunnel Overlay IPs

#### IPsec (FortiGate SD-WAN)

| Tunnel | FG1 IP | FG2 IP | Subnet |
|--------|--------|--------|--------|
| MPLS-VPN | 10.254.1.1 | 10.254.1.2 | /24 |
| SASE-VPN | 10.255.2.1 | 10.255.2.2 | /24 |

#### WireGuard (POP-to-POP over Internet)

| Tunnel | CF-POP1 IP | CF-POP2 IP | Subnet |
|--------|------------|------------|--------|
| wg0 | 10.255.0.1 | 10.255.0.2 | /24 |

---

**Architecture Layers:**
- **Underlay:** MPLS L3VPN (CE-PE-PE-CE)
- **Overlay:** SD-WAN with dual-path IPsec tunnels
- **Security:** SASE (SWG, ZTNA, DNS filtering)

**【日本語サマリ】**

MPLS L3VPNをUnderlayとし、SD-WAN（デュアルパスIPsec）をOverlay、SASE（SWG、ZTNA、DNSフィルタリング）をセキュリティ層として統合した検証環境。

---

## 🎯 Current Focus

- **ENSDWI (300-415) preparation** — building on ENARSI-level routing concepts already studied
- **Cisco Viptela SD-WAN integration (No vManage)** — OMP routing, IPsec tunnels, and control-plane behavior validation
- **Dual-path failover verification** — MPLS primary / SASE secondary with SLA-based path switching and AS-path prepending
- **ZTNA design evaluation (planned)** — connector-based access to AWS EC2 via Twingate

**【日本語サマリ】**

ENARSIレベルのルーティング概念を学習済み。現在、設計・構築案件を想定しENSDWI (300-415) を検討中。Cisco Viptela SD-WAN（vManageなし構成）をラボで構築し、OMPルーティングやIPsecトンネルの挙動を検証。SD-WANとSASE接続時の経路選択やフェイルオーバー挙動を中心に検証を実施。ZTNA（Twingate）を用いたAWS EC2への接続設計・検証も計画中。

---

## 📫 Contact

- **Location:** Tokyo,Yokohama, Japan
- **LinkedIn:** [Connect with me](#)

---

*Bridging traditional enterprise networking with modern SASE architectures*
