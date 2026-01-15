# 1. Response
- **[Preparation, Detecion, Analysis, containment, eradication, recovery, lesson learned] IR Cycle**
- security information and event management (SIEM), security orchestration, automation and response (SOAR)
- computer incident response team (CIRT), computer emergency reponse tean(CERT), security operation center(SOC)
"using out-of-band communication. using corperate email runs the risk"
"new attack that the attacker could launch through information they have gained about the network."

# 2. Forensics
- **[Due process, Legal hold]**, fair

# 3. Data
- Syslog [PRI primary code, header, messaeg]
- Logs {Host OS, Application, Endpoint}
- email [mail user agent > mail delivery agent > message trasfer agent(EX: SMTP Server, mail security gateway)]

# 4. Tools
- [agent-base, listener/collector, sensor] collection
- **retrospective network analysis** at {header, payload} level, **single pane of glass analysis** (SIEM)
- Netflow > IP Flow Information Export (IPFOX) IETF standard, charasteristic/key [src add, dst add, protocal, src port, dst port] (+[input interface, IP type for service])
- Security Conten Automation Protocal (SCAP), Open Vulnerability and assessment language (OVAL), Extensible Configuration Chekclist Description format (XCCDF)
- **flow collector(metadata and statistic about traffic), network monitor(CPU/Memory load, dus, net utilization), heartbeat message(availability)**

**achieving** in IR cycle
q8, q13, q14, q15, q16, q20, q25, q27