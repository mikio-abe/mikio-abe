CCNP ENCOR certified Network Engineer with expertise in **SASE, SD-WAN, and Zero Trust architectures**, built on a strong foundation of enterprise and service provider networking.

**【日本語サマリ】**

CCNP ENCOR取得済みのネットワークエンジニア。SASE、SD-WAN、ゼロトラストアーキテクチャを専門とし、エンタープライズおよびサービスプロバイダーネットワークの経験を基盤としています。

---

## 🛠 Technical Skills

| Category | Skills |
|----------|--------|
| SASE / Zero Trust | Cloudflare Zero Trust (SWG, ZTNA, WARP) |
| SD-WAN | FortiGate SD-WAN, Cisco Viptela (vBond/vSmart/vEdge), IPsec/VRF integration |
| NGFW | Palo Alto PA-VM (PAN-OS), IPSec VPN, BGP over IPSec, App-ID |
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
| **NGFW (Palo Alto)** | IPSec VPN, BGP over IPSec, App-ID, MPLS/SASE Failover | [View →](https://github.com/mikio-abe/NGFW-Palo-Alto)|
| **Enterprise / SP** | MPLS L3VPN, BGP Policy, VRF Design | [View →](https://github.com/mikio-abe/Enterprise-SP) |
| **Troubleshooting** | Encrypted Tunnel Analysis, Visibility Boundaries | [View →](https://github.com/mikio-abe/Troubleshooting) |
| **Lab vs Production** | Differences between lab and production deployments | [View →](https://github.com/mikio-abe/Lab-vs-Production) |

**【日本語サマリ】**

各コンポーネントはハンズオン実装とアーキテクチャドキュメントで構成。SASE/Zero Trust、SD-WAN（FortiGate/Cisco Viptela）、NGFW（Palo Alto）、Enterprise/SP（MPLS）、Troubleshooting、Lab vs Productionの7つのリポジトリで詳細を公開。

---

## 🔬 Lab Overview

### SASE × SD-WAN Verification Lab

A comprehensive verification environment integrating MPLS underlay, SD-WAN overlay, and SASE security layers.<BR>

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/8c2a2b9b-bf74-4b62-83a8-ca9e20dd252f" />

This diagram shows a multi-vendor SASE/SD-WAN lab in EVE-NG connected to real ISP lines. <BR>
Two WAN paths — MPLS closed network and SASE IPSec tunnel via internet — run in parallel, with priority-based failover configured between them. <BR>
Linux POPs bridge the virtual lab and real ISP connections, tunneling outbound to Cloudflare Zero Trust over live broadband and mobile tethering.

**【日本語サマリ】**<BR>
EVE-NG上のマルチベンダーSASE/SD-WANラボと実ISP回線を組み合わせた構成図です。
MPLS閉域網とインターネット経由のSASE IPSecトンネルの2経路を並列で構成し、プライオリティによる自動切替を実装しています。<BR>
Linux POPが仮想ラボと実回線の境界を橋渡しし、固定ブロードバンドとモバイルテザリングでCloudflare Zero Trustに接続しています。

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
