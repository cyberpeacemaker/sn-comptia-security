# 1. Network Architecture
- [network infrastructure, network app, data assets]
- on-premise network (enterprise LAN)
- VLAN, security zone, 
- 802.1x (Port-based Network Access) < [Extensible Authenitcation Protocal(**EAP**), Remote Authentication Dia-In User Service(**RADIUS**)]
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

q2, q4, q5, q6, q13, q15, q20
**EAP**