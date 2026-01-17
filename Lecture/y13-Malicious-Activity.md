# 1. Malware
- payload [spyware, rootkit, remote access Trojan (RAT), ransomware]
- computer vireus [non-resident/file infector, memory resident, boot, script and marco]
- fileless [memory-resident (DLL), shellcode, live off the land (PowerShell, Window Management Instrumentation)]
- [supercookies, beacon], C2 covert Channel [Internt Relay Chat, embeded in HTTPS/DNS]
- Trojan > System-level privilege - **Rootkit**
- **Indicator of Compromise (IOC)** is evidence of a Tatic, technique, procedure (TTP)
- **data loss prevention (DLP)** also log **blocked content event**

# 2. Physicla and Netowrk
- **bloatware**, **Potentially Unwanted Program (PUP)**
- **Heating Ventilation Air Condition (HVAC)** room
- Radio Frequency ID (RFID) {cloning, Skimming}
- DoS (Reflected, )
- DNS [on-path, cliet, server]
- rogue ap > masquerading as legitmate > evil twin, disassociation attack
- Local Security Authority Subsystem Service (**LSASS**), Security Account Manager (**SAM**) database cahed in momory, lsass.exe > **Credential Reply**, Pass the ticket (PtT) [goldern/silver ticket]
"Where they remain a risk, a detection system can be configured to correlate a sequence of security log events, but this method can be prone to false positives. Antivirus and host-based intrusion detection can often detect the malware code used to dump credentials or launch ticket forgery attacks."
- **collision attack** > forge digital certificate > [spoof trusted website, malware from trusted publisher]
- Persistence [AutoRun kye, scheduled task, Windows Management Intrumnetation(WMI) event subsription]

# 3. Application
- Seesion [replay attack, forgery attack{cross-site request forgery CSRF(confused deputy attack)/server-side request forgery **SSRF**}]
- **canonicalization** attack, RUL Analysis (**starting point**), percent encoding

