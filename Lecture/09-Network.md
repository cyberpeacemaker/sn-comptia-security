# 1. Baseline
- CIS Benchmark, Security Technical Implementation Guides (STIGs) < Defense Information Systems Agency (DISA) 
- puppet, chef, ansible, microsoft group policy
- OpenSCAP, CIS-CAT Pro toll, SCAP Compliance Checker
- unnecesasry [service, app], Privileged Access Management(PAM)
- wireless [WPA3 (encrypted), **RADIUS** (**authentication**)], patchy converage > [rogue, evil twin], [site survey, heatmap], [BSSID, SSID]
- Easy connect method (Device Provisioning Protocal **DPP**) > [QR, NFC] public/private key pair
- **Wi-Fi 6 (802.11ax), Wi-Fi 5 (802.11ac), Wi-Fi 4 (802.11n)**
- [WPA2, pre-shared key, pairwise Mater key(PMK)], [WPA3, Simultaneous authentication of Equals (SAE)], Extensible Authentication Protocal (**EAP**), RADIUS [EAP over LAN (EAPoL)]
- VLAN + **NAC** > dynamic VLAN assigenment, NAC {agent/agnetless}configuration

# 2. Enhancement
- firewall [block incoming from internal or private IP, protocal that should only function at LAN]
- screened subnet (DMZ)
- detection method [signature/pattern, behavioral/anomaly (ML or handcraft), trend (overtime)]
- web filter {agent-based(with cloud platform)/centralized web}

**802.1x**
**Simultaneous Authentication of Equals**
q2, q9, q12