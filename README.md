# Hi, I'm Mikio Abe

CCNP ENCOR certified Network Engineer with expertise in **SASE, SD-WAN, and Zero Trust architectures**, built on a strong foundation of enterprise and service provider networking.

**【日本語サマリ】**

CCNP ENCOR取得済みのネットワークエンジニア。SASE、SD-WAN、ゼロトラストアーキテクチャを専門とし、エンタープライズおよびサービスプロバイダーネットワークの経験を基盤としています。

---

## 🛠 Technical Skills

**SASE / Zero Trust:** Cloudflare Zero Trust (SWG, ZTNA, WARP)
**SD-WAN:** FortiGate SD-WAN, IPsec/VRF integration
**Networking:** MPLS L3VPN, BGP, OSPF, EIGRP, VRF
**VPN Technologies:** IPsec, WireGuard, DMVPN, GRE
**Service Provider:** MPLS, BGP VPNv4, LDP
**Tools:** EVE-NG Pro, Wireshark, TCPDump, GNS3
**Certifications:** CCNP ENCOR | Fortinet NSE4 (Preparing)

**【日本語サマリ】**

Cloudflare Zero Trust、FortiGate SD-WAN、MPLS L3VPN、各種VPN技術（IPsec、WireGuard、DMVPN）を習得。EVE-NG Pro等のラボ環境で検証実施。CCNP ENCOR取得済み、Fortinet NSE4準備中。

---

## 🔬 Lab Overview

### SASE × SD-WAN Verification Lab

A comprehensive verification environment integrating MPLS underlay, SD-WAN overlay, and SASE security layers.

```
Site A                                              Site B
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

**【日本語サマリ】**

MPLS L3VPNをUnderlayとし、SD-WAN（デュアルパスIPsec）をOverlay、SASE（SWG、ZTNA、DNSフィルタリング）をセキュリティ層として統合した検証環境。

---

## 🚀 Key Components

Each component demonstrates hands-on implementation with architectural documentation:

| Component | Description | Details |
|-----------|-------------|---------|
| **SASE / Zero Trust** | SWG, ZTNA, TLS Inspection, DNS Filtering | [View →](https://github.com/mikio-abe/SASE-ZeroTrust) |
| **SD-WAN** | Dual-path Design, Health Check, SLA-based Failover | [View →](https://github.com/mikio-abe/SD-WAN) |
| **Enterprise / SP** | MPLS L3VPN, BGP Policy, VRF Design | [View →](https://github.com/mikio-abe/Enterprise-SP) |
| **Troubleshooting** | Encrypted Tunnel Analysis, Visibility Boundaries | [View →](https://github.com/mikio-abe/Troubleshooting) |

**【日本語サマリ】**

各コンポーネントはハンズオン実装とアーキテクチャドキュメントで構成。SASE/Zero Trust、SD-WAN、Enterprise/SP（MPLS）、Troubleshootingの4つのリポジトリで詳細を公開。

---

## 🎯 Current Focus

- **Fortinet NSE4 certification** - Preparing for exam
- **Mobile endpoint verification** - Testing Slack/Teams through SASE to verify OAuth redirect, WebSocket connectivity, and TLS inspection compatibility
- **Twingate ZTNA evaluation** - Connector-based access to AWS EC2 instances
- *(Optional: Zscaler ZDTA certification)*

**【日本語サマリ】**

Fortinet NSE4取得準備中。スマホにSlack/Teams等をインストールし、SASE経由での認証（OAuthリダイレクト）、WebSocket通信、TLS Inspectionの互換性を検証予定。TwingateのConnector型ZTNAでAWS EC2への接続検証も計画中。

---

## 📫 Contact

- **Location:** Tokyo, Japan
- **LinkedIn:** [Connect with me](#)

---

*Bridging traditional enterprise networking with modern SASE architectures*
