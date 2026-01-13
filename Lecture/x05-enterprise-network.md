# 1. Network Architecture
- [network infrastructure, network app, data assets]
- on-premise network (enterprise LAN)
- VLAN, security zone, 
- **802.1x (Port-based Network Access)** < [Extensible Authenitcation Protocal(**EAP**), Remote Authentication Dia-In User Service(**RADIUS**)]
- 5.1.17 VIDEO

# 2. Security Appliance
- Test Access Point (TAP), Switched Port Analyzer (SPAN) / mirror port
- app firewall [routed, bridged, inline], transparent mode, state table
- forward/reverse proxy server, transparent(forced, intercepting)
- load balancer [layer4m layer7(content switch)], [heartbeat, health check], session affinity
- web application firewall (WAF)

# 3. Secure Communication
- VPN (telecommuter), site-to-site, PPTP(deprecated), [SSL, TLS, IPsec]
- TLS > Certificate
- IPsec (Layer 3), [Authentication Header(AH), Encapsulating Security Payload(ESP)]
- Internet key exchange(IKE), security assoiciation(SA), IKEv2[easier, MOBIKE]
- RDP, HTML5 VPN (WebSocket)
- secure administrative workstations(SAWs) [out-of-band, jump server]

q6, q8, q14, q19, q21

---

To understand the relationship between **VPN**, **TLS**, and **IPsec**, it helps to think of them as a "Goal" versus the "Tools" used to achieve it.

A **VPN (Virtual Private Network)** is a concept or a service. **IPsec** and **TLS** are the technical protocols (the "languages" and "encryption rules") used to build that VPN.

---

### 1. The Core Relationship

A VPN is simply a secure "tunnel" through the internet. To build that tunnel, engineers use one of two primary toolsets:

| Protocol | OSI Layer | Common VPN Type | Typical Use Case |
| --- | --- | --- | --- |
| **IPsec** | **Layer 3** (Network) | Site-to-Site VPN | Connecting two offices (e.g., London to NY). |
| **TLS** | **Layer 7** (Application) | Remote Access VPN | A remote worker logging into a company portal via a browser. |

---

### 2. IPsec: The "Whole Network" Guard

**IPsec (Internet Protocol Security)** works at the network level. It doesn't care which app you are using (Email, Zoom, Web); it encrypts **every single packet** leaving your device.

* **How it works:** It authenticates and encrypts the entire IP packet, including the header.
* **Best for:** "Always-on" connections between buildings or full-device encryption where you want the user to feel like they are physically plugged into the office wall.
* **The Catch:** Usually requires special software (a VPN client) installed on the computer.

---

### 3. TLS: The "Browser-Friendly" Guard

**TLS (Transport Layer Security)**—the successor to SSL—is what you use every time you visit a website starting with `https://`. In a VPN context, it’s much more surgical.

* **How it works:** It secures the connection between a specific application (like your browser) and a server.
* **Best for:** "Clientless" VPNs. You just open Chrome, go to a login page, and you’re in. You don't need to install a heavy app.
* **The Catch:** It’s great for web-based apps but can be trickier to use for non-web traffic (like legacy file shares) without extra configuration.

---

### 4. Can they be used together?

**Yes, and they often are.** This is known as **"Layered Security."**

Imagine you are a remote worker:

1. You turn on your **IPsec VPN** to create a secure tunnel to your company's network. (The "bad guys" on the coffee shop Wi-Fi now see only encrypted junk).
2. Inside that tunnel, you go to your company's HR portal using **HTTPS (which uses TLS)**.

Now you have two layers of encryption. If the IPsec tunnel were somehow breached, your sensitive HR data is still protected by TLS.

---

> **Summary:** **VPN** is the secure tunnel. **IPsec** is a heavy-duty protocol that secures the whole network. **TLS** is a flexible protocol that secures specific applications and web traffic.
