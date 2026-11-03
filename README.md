# 🦉 Owl OS

<p align="center">
  <img src="assets/owl-os-logo.png" alt="Owl OS logo" width="160"/>
</p>

<p align="center"><strong>Owl OS</strong> — Debian-based cybersecurity OS with 275+ open-source offensive, defensive &amp; intelligence tools</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Tools-275%2B-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Website-owlsec.org-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Base-Debian-a80000?style=flat-square"/>
</p>

---

## Desktop

<p align="center">
  <img src="assets/owl-os-desktop.jpg" alt="Owl OS desktop" width="720"/>
</p>

---

## Why Owl OS

- **275+ native tools** — recon, web, network, AD, cloud, forensics, hardening, wireless, crypto, OSINT and more
- **Debian-based** — familiar apt workflow, stable base, easy to extend
- **Offensive + defensive + intelligence** — one toolkit for red, blue and intel work
- **Install anywhere** — use the ISO, or add the Owl apt repo on Debian/Ubuntu

---

## Download

- **ISO:** [https://owlsec.org/downloads/owl.iso](https://owlsec.org/downloads/owl.iso)
- **Size:** `owl.iso` — 9,758,382,080 bytes (9.09 GiB / 9.76 GB)
- **Download page:** [https://owlsec.org/download](https://owlsec.org/download)
- **SHA256:** `828c6405873b0728dac70099d154dd33e4fae0c76bf892511e6081888b8e1d06`

```bash
# Verify the ISO (should print: owl.iso: OK)
echo "828c6405873b0728dac70099d154dd33e4fae0c76bf892511e6081888b8e1d06  owl.iso" | sha256sum -c -
```

---

## Verify your download

- **File:** `owl.iso` (Owl OS 1.0 "Athena")
- **Size:** 9,758,382,080 bytes (9.8 GB)
- **SHA256:** `828c6405873b0728dac70099d154dd33e4fae0c76bf892511e6081888b8e1d06`

Verify on Linux:

```bash
sha256sum owl.iso
```

---

## Install tools on any Debian/Ubuntu

```bash
curl -fsSL https://owlsec.org/repo/owl-os-archive-keyring.gpg | sudo tee /usr/share/keyrings/owl-os-archive-keyring.gpg >/dev/null
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/owl-os-archive-keyring.gpg] https://owlsec.org/repo/ owl-os main" | sudo tee /etc/apt/sources.list.d/owl-os.list
sudo apt update && sudo apt install owl-system
```

---

## Tools

### Recon/Scanning (4)

| Tool | Description |
| --- | --- |
| [OApkscan](https://github.com/owlsecx/OApkscan) | APK / IPA Static Analysis Engine v2.0 covering Permissions , Secrets , Malware , Obfuscation , Certs , Entropy. |
| [OATTACK](https://github.com/owlsecx/OATTACK) | Pentest Toolkit for authorized security testing and analysis. |
| [OBinScope](https://github.com/owlsecx/OBinScope) | Static Executable Triage Analyzer for authorized security testing and analysis. |
| [OGet](https://github.com/owlsecx/OGet) | Secure Multi-File Downloader for authorized security testing and analysis. |

### Web (29)

| Tool | Description |
| --- | --- |
| [OApiScan](https://github.com/owlsecx/OApiScan) | REST / GraphQL API Security Auditor for authorized security testing and analysis. |
| [OBalancer](https://github.com/owlsecx/OBalancer) | Load Balancing & Infrastructure Detector: Detect DNS LB, HTTP LB, CDN, WAF, TLS, GeoIP. |
| [OBlast](https://github.com/owlsecx/OBlast) | Detect and confirm OS command injection via GET/POST/Header vectors. Echo-marker output extraction, time-based. |
| [OBreak](https://github.com/owlsecx/OBreak) | Authorised HTTP login-form credential testing. GET/POST/JSON , Failure & success detection , Response-length. |
| [OBurrow](https://github.com/owlsecx/OBurrow) | LFI Hunter for authorized security testing and analysis. |
| [OCockpitX](https://github.com/owlsecx/OCockpitX) | Cockpit Web Console Configuration Auditor for authorized security testing and analysis. |
| [OCookieX](https://github.com/owlsecx/OCookieX) | Cookie Security Analyzer & Session Auditor for authorized security testing and analysis. |
| [ODirHunt](https://github.com/owlsecx/ODirHunt) | Multi-threaded web crawler — endpoint discovery, sitemap/robots parsing, header & tech fingerprinting, form. |
| [ODive](https://github.com/owlsecx/ODive) | Deep LFI/RFI/traversal detection. Built-in paths, expanded PHP wrappers, log poisoning, RFI module, confidence. |
| [OFuzzX](https://github.com/owlsecx/OFuzzX) | HTTP Parameter & Path Fuzzer for authorized security testing and analysis. |
| [OGuacX](https://github.com/owlsecx/OGuacX) | Apache Guacamole Gateway Configuration Auditor for authorized security testing and analysis. |
| [OHaproxyX](https://github.com/owlsecx/OHaproxyX) | HAProxy Load-Balancer Configuration Auditor for authorized security testing and analysis. |
| [OHeaders](https://github.com/owlsecx/OHeaders) | Security Headers Auditor for authorized security testing and analysis. |
| [OHttpdX](https://github.com/owlsecx/OHttpdX) | Web-Server Configuration Auditor for authorized security testing and analysis. |
| [OJwtX](https://github.com/owlsecx/OJwtX) | JWT / JWS / JWE Security Auditor for authorized security testing and analysis. |
| [OLiteSpeedX](https://github.com/owlsecx/OLiteSpeedX) | OpenLiteSpeed / LiteSpeed Configuration Auditor for authorized security testing and analysis. |
| [OMatrixX](https://github.com/owlsecx/OMatrixX) | Matrix Synapse Configuration Auditor for authorized security testing and analysis. |
| [ONextcloudX](https://github.com/owlsecx/ONextcloudX) | Nextcloud / ownCloud Configuration Hardening Auditor for authorized security testing and analysis. |
| [OPassForce](https://github.com/owlsecx/OPassForce) | Auth-flow audit, rate-limit / WAF detection, CSRF analysis, cookie inspection, response heuristics. |
| [OPhpIni](https://github.com/owlsecx/OPhpIni) | PHP Runtime Configuration Hardening Auditor for authorized security testing and analysis. |
| [OSerial](https://github.com/owlsecx/OSerial) | Insecure Deserialization Auditor for authorized security testing and analysis. |
| [OSpiderX](https://github.com/owlsecx/OSpiderX) | BFS web crawling, JS rendering, link extraction, sitemap generation, login support, URL probing. |
| [OSQL](https://github.com/owlsecx/OSQL) | Professional SQL Injection Scanner for authorized security testing and analysis. |
| [OSquidX](https://github.com/owlsecx/OSquidX) | Squid Proxy Configuration Hardening Auditor for authorized security testing and analysis. |
| [OTomcatX](https://github.com/owlsecx/OTomcatX) | Apache Tomcat Configuration Auditor for authorized security testing and analysis. |
| [OTraefikX](https://github.com/owlsecx/OTraefikX) | Modern Reverse-Proxy Configuration Auditor for authorized security testing and analysis. |
| [OWeb](https://github.com/owlsecx/OWeb) | OWeb — Web Recon & Security Analysis Suite for authorized security testing. |
| [OWebShell](https://github.com/owlsecx/OWebShell) | Web Shell & Backdoor Detector for authorized security testing and analysis. |
| [OWpConfX](https://github.com/owlsecx/OWpConfX) | WordPress Installation Configuration Auditor for authorized security testing and analysis. |

### Network (49)

| Tool | Description |
| --- | --- |
| [OAnonFtp](https://github.com/owlsecx/OAnonFtp) | Read-only auditor that checks FTP servers for anonymous account access. |
| [OARPX](https://github.com/owlsecx/OARPX) | ARP Spoof / MiTM + DNS Spoof Suite: ARP poisoning, DNS spoofing, recon, live monitor. |
| [OBandwidth](https://github.com/owlsecx/OBandwidth) | OBandwidth is a bandwidth and throughput monitor that tracks per-interface traffic from /proc/net/dev, runs… |
| [OBannerGrab](https://github.com/owlsecx/OBannerGrab) | Multi-threaded banner grabbing with active service probing, SSL/TLS fingerprinting, CVE hints, port-range parsing. |
| [OBGP](https://github.com/owlsecx/OBGP) | OBGP is a BGP route and RPKI analyzer that audits exported BGP tables for hijacks, bogons, MOAS conflicts, AS-path… |
| [OBindX](https://github.com/owlsecx/OBindX) | Offline DNS Server Configuration Auditor for authorized security testing and analysis. |
| [OBruteSSH](https://github.com/owlsecx/OBruteSSH) | Professional multi-mode SSH security audit framework with adaptive threading, smart rate-limiting, CIDR/range. |
| [OCANBus](https://github.com/owlsecx/OCANBus) | OCANBus is a defensive CAN bus analysis lab that decodes vehicle CAN captures with DBC files, profiles bus traffic,… |
| [OChisel](https://github.com/owlsecx/OChisel) | Craft, inspect, decode, replay and capture raw TCP / UDP / ICMP / ARP / IPv6 packets. Accurate checksum. |
| [OConns](https://github.com/owlsecx/OConns) | OConns is a socket and connection inspector that lists TCP/UDP sockets with their owning processes, monitors… |
| [OCraftX](https://github.com/owlsecx/OCraftX) | Build, inspect, decode, and send raw network frames ARP / ICMP / TCP / UDP / Custom — with live capture, hex. |
| [ODhcpX](https://github.com/owlsecx/ODhcpX) | Offline DHCP / IPv6-RA Server Config Auditor for authorized security testing and analysis. |
| [ODNSHunt](https://github.com/owlsecx/ODNSHunt) | ODNSHunt — Fast DNS Subdomain Enumerator for authorized security testing. |
| [ODNSHuntX](https://github.com/owlsecx/ODNSHuntX) | Multi-threaded subdomain enumeration, DNSSEC validation, wildcard detection, DNS record analysis, zone transfer. |
| [ODovecotX](https://github.com/owlsecx/ODovecotX) | Dovecot IMAP / POP3 Configuration Auditor for authorized security testing and analysis. |
| [OEcho](https://github.com/owlsecx/OEcho) | Multi-threaded ICMP ping sweep across IP ranges or CIDRs. Detects live hosts, measures latency, resolves hostnames. |
| [OFlow](https://github.com/owlsecx/OFlow) | Network Flow / Connection Session Analyzer for authorized security testing and analysis. |
| [OFtpdX](https://github.com/owlsecx/OFtpdX) | FTP Server Configuration Hardening Auditor for authorized security testing and analysis. |
| [OICS](https://github.com/owlsecx/OICS) | ICS / SCADA / OT Offline Security Auditor for authorized security testing and analysis. |
| [OKeepaliveX](https://github.com/owlsecx/OKeepaliveX) | keepalived (VRRP / LVS) Configuration Auditor for authorized security testing and analysis. |
| [OMailSec](https://github.com/owlsecx/OMailSec) | Email-Domain Authentication Auditor for authorized security testing and analysis. |
| [OMqttX](https://github.com/owlsecx/OMqttX) | IoT Message-Broker Configuration Auditor for authorized security testing and analysis. |
| [ONetwatch](https://github.com/owlsecx/ONetwatch) | Network MITM, ARP and packet sentinel for live LAN monitoring on Owl OS. |
| [ONfsAudit](https://github.com/owlsecx/ONfsAudit) | Offline NFS Export Configuration Auditor for authorized security testing and analysis. |
| [ONode](https://github.com/owlsecx/ONode) | DNS , Local/Public IP , Port Scan , Whois , Ping , Traceroute , SSL/TLS , GeoIP , HTTP Headers , CIDR calc . |
| [OPdnsX](https://github.com/owlsecx/OPdnsX) | PowerDNS Configuration Hardening Auditor for authorized security testing and analysis. |
| [OPoison](https://github.com/owlsecx/OPoison) | ARP spoof and MITM detection engine for monitoring, scanning, alerting and forensics. |
| [OPortX](https://github.com/owlsecx/OPortX) | Port Scanner for authorized security testing and analysis. |
| [OProxy](https://github.com/owlsecx/OProxy) | Proxy intelligence framework for checking anonymity, GeoIP, speed and bulk proxy validation. |
| [Orbit](https://github.com/owlsecx/Orbit) | Strategic Network Reconnaissance for authorized security testing and analysis. |
| [ORelay](https://github.com/owlsecx/ORelay) | Bidirectional TCP bridge, port forwarding, traffic inspection, multi-client relay, packet capture, protocol analysis. |
| [ORouteX](https://github.com/owlsecx/ORouteX) | ORouteX — Routing Protocol Attack Suite for authorized security testing. |
| [OSmtpX](https://github.com/owlsecx/OSmtpX) | Offline SMTP / MTA Config Auditor for authorized security testing and analysis. |
| [OSniffer](https://github.com/owlsecx/OSniffer) | Defensive network monitor for DNS/HTTP/TLS/SSH and scan detection with GeoIP reports. |
| [OSnmp](https://github.com/owlsecx/OSnmp) | Ultra-fast parallel SNMP scanning, community brute-force, OID walk, system enumeration. |
| [OSnmpdX](https://github.com/owlsecx/OSnmpdX) | Net-SNMP Agent Configuration Auditor for authorized security testing and analysis. |
| [OSpecter](https://github.com/owlsecx/OSpecter) | Multi-mode port scanning, service fingerprinting, OS detection, CVE hints, scripted probes, network sweep. |
| [OStamp](https://github.com/owlsecx/OStamp) | Service detection , Banner grab , TLS intel , OS fingerprint. |
| [OSurge](https://github.com/owlsecx/OSurge) | ICMP / TCP / UDP crafting, traceroute, latency measurement, firewall rule validation. |
| [OSweep](https://github.com/owlsecx/OSweep) | Network Host Discovery & Live Sweep for authorized security testing and analysis. |
| [OTelProbe](https://github.com/owlsecx/OTelProbe) | Telnet security audit suite for credential checks, banner grab and CVE probing. |
| [OTftpX](https://github.com/owlsecx/OTftpX) | TFTP & PXE Network-Boot Server Config Auditor for authorized security testing and analysis. |
| [OTraceX](https://github.com/owlsecx/OTraceX) | Advanced TCP Path Tracer: TCP session-based traceroute through firewalls. |
| [OTrack](https://github.com/owlsecx/OTrack) | Advanced network reconnaissance and diagnostics for systems you own or are authorized to test. |
| [OUnboundX](https://github.com/owlsecx/OUnboundX) | Unbound DNS Resolver Hardening Auditor for authorized security testing and analysis. |
| [OVector](https://github.com/owlsecx/OVector) | Host discovery, DNS recon, NDP analysis, traffic analysis, exploit testing, address utilities. |
| [OVendors](https://github.com/owlsecx/OVendors) | ARP Analysis & MAC Fingerprinting: ARP scan, vendor lookup, conflict detection. |
| [OVoipX](https://github.com/owlsecx/OVoipX) | VoIP / RTC Server Configuration Auditor for authorized security testing and analysis. |
| [OZone](https://github.com/owlsecx/OZone) | DNS records, zone transfer, subdomain brute force, wildcard detection, takeover check, DNSSEC, reverse DNS, open. |

### Active Directory (13)

| Tool | Description |
| --- | --- |
| [OAD](https://github.com/owlsecx/OAD) | Active Directory Offline Auditor for authorized security testing and analysis. |
| [OAuthX](https://github.com/owlsecx/OAuthX) | OAuth 2.0 / OpenID Connect Config Auditor for authorized security testing and analysis. |
| [OBloodMap](https://github.com/owlsecx/OBloodMap) | OBloodMap is a defensive Active Directory attack-path mapper that analyzes BloodHound exports offline to rank the… |
| [OIpaX](https://github.com/owlsecx/OIpaX) | FreeIPA / Red Hat IdM Server Configuration Auditor for authorized security testing and analysis. |
| [OKeycloakX](https://github.com/owlsecx/OKeycloakX) | Offline Keycloak Realm Export & Server Config Auditor for authorized security testing and analysis. |
| [OLdapX](https://github.com/owlsecx/OLdapX) | Offline LDAP / Directory Config Auditor for authorized security testing and analysis. |
| [OPamAudit](https://github.com/owlsecx/OPamAudit) | Offline Linux PAM Auditor for authorized security testing and analysis. |
| [ORadiusX](https://github.com/owlsecx/ORadiusX) | Offline AAA / RADIUS Server Configuration Auditor covering FreeRADIUS 2.x / 3.x │ radiusd │ raddb trees; Clients │. |
| [OSaml](https://github.com/owlsecx/OSaml) | SAML / SSO / OIDC Configuration Auditor for authorized security testing and analysis. |
| [OSmbScan](https://github.com/owlsecx/OSmbScan) | SMB / NetBIOS Exposure Scanner for authorized security testing and analysis. |
| [OSssdX](https://github.com/owlsecx/OSssdX) | Offline SSSD / NSS / realmd Client Auditor for authorized security testing and analysis. |
| [OSudoAudit](https://github.com/owlsecx/OSudoAudit) | Offline Sudoers Policy Auditor for authorized security testing and analysis. |
| [Overlord](https://github.com/owlsecx/Overlord) | Advanced SMB Enumeration Framework: SMB enum , risk scoring , MITRE , SIEM output. |

### Cloud/Containers (27)

| Tool | Description |
| --- | --- |
| [OAnsibleX](https://github.com/owlsecx/OAnsibleX) | Ansible Security Linter (Offline) for authorized security testing and analysis. |
| [OArgoX](https://github.com/owlsecx/OArgoX) | GitOps Controller Security Auditor for authorized security testing and analysis. |
| [OCephX](https://github.com/owlsecx/OCephX) | Ceph Storage Cluster Configuration Auditor for authorized security testing and analysis. |
| [OCiPipe](https://github.com/owlsecx/OCiPipe) | Offline CI/CD Pipeline Security Linter for authorized security testing and analysis. |
| [OCloudCfg](https://github.com/owlsecx/OCloudCfg) | Cloud IaC & Config Security Auditor for authorized security testing and analysis. |
| [OConsulX](https://github.com/owlsecx/OConsulX) | Service-Discovery / Distributed KV Config Auditor for authorized security testing and analysis. |
| [OContainer](https://github.com/owlsecx/OContainer) | Docker / OCI Container Security Auditor for authorized security testing and analysis. |
| [OContainerEsc](https://github.com/owlsecx/OContainerEsc) | OContainerEsc is a defensive container escape auditor that checks Docker/Podman inspect output, Kubernetes pod… |
| [ODockerFile](https://github.com/owlsecx/ODockerFile) | Dockerfile & Compose Security Linter for authorized security testing and analysis. |
| [OEtcdX](https://github.com/owlsecx/OEtcdX) | etcd Key-Value Store Configuration Auditor for authorized security testing and analysis. |
| [OGiteaX](https://github.com/owlsecx/OGiteaX) | Gitea / Forgejo Configuration Auditor for authorized security testing and analysis. |
| [OGitlabX](https://github.com/owlsecx/OGitlabX) | GitLab Self-Managed / Omnibus Config Auditor for authorized security testing and analysis. |
| [OGitSec](https://github.com/owlsecx/OGitSec) | Git Repository Secret & History Auditor for authorized security testing and analysis. |
| [OGitSrv](https://github.com/owlsecx/OGitSrv) | Self-Hosted Git Server Auditor for authorized security testing and analysis. |
| [OGlusterX](https://github.com/owlsecx/OGlusterX) | GlusterFS Configuration Hardening Auditor for authorized security testing and analysis. |
| [OHarborX](https://github.com/owlsecx/OHarborX) | Harbor Container Registry Server Config Auditor for authorized security testing and analysis. |
| [OJenkinsX](https://github.com/owlsecx/OJenkinsX) | Offline Jenkins Controller Auditor for authorized security testing and analysis. |
| [OJupyterX](https://github.com/owlsecx/OJupyterX) | Jupyter Notebook / Lab / Hub Config Auditor for authorized security testing and analysis. |
| [OK8sRbac](https://github.com/owlsecx/OK8sRbac) | Offline Kubernetes RBAC & Privilege-Path Analyzer for authorized security testing and analysis. |
| [OLibvirtX](https://github.com/owlsecx/OLibvirtX) | KVM / QEMU / libvirt Hypervisor Auditor for authorized security testing and analysis. |
| [OMinioX](https://github.com/owlsecx/OMinioX) | Self-Hosted S3 Storage Security Auditor for authorized security testing and analysis. |
| [ONexusX](https://github.com/owlsecx/ONexusX) | Sonatype Nexus Repository Manager Config Auditor for authorized security testing and analysis. |
| [ONomadX](https://github.com/owlsecx/ONomadX) | HashiCorp Nomad Security Auditor for authorized security testing and analysis. |
| [OPuppetX](https://github.com/owlsecx/OPuppetX) | Puppet Configuration-Hardening Auditor for authorized security testing and analysis. |
| [ORegTrust](https://github.com/owlsecx/ORegTrust) | Container Image Trust & Registry Auditor for authorized security testing and analysis. |
| [OSaltX](https://github.com/owlsecx/OSaltX) | SaltStack Configuration-Hardening Auditor for authorized security testing and analysis. |
| [OStackX](https://github.com/owlsecx/OStackX) | OpenStack Service Configuration Security Auditor for authorized security testing and analysis. |

### Forensics (37)

| Tool | Description |
| --- | --- |
| [OAmcache](https://github.com/owlsecx/OAmcache) | OAmcache is a Windows Amcache forensics tool with a native registry hive parser that extracts execution evidence,… |
| [OBeacon](https://github.com/owlsecx/OBeacon) | OBeacon is a C2 beacon hunter that finds hosts calling home on a timer by scoring connection regularity in proxy,… |
| [OBinwalk](https://github.com/owlsecx/OBinwalk) | Magic signatures , entropy , PE/ELF/Mach-O parser strings , IOC extraction , polyglot detection YARA-like rules . |
| [OBiopsy](https://github.com/owlsecx/OBiopsy) | Advanced Digital Forensics & Intelligence Suite. |
| [OByteForge](https://github.com/owlsecx/OByteForge) | OByteForge is a binary analysis workbench for hex viewing, searching, string and IOC extraction, entropy analysis,… |
| [OC2](https://github.com/owlsecx/OC2) | OC2 is a defensive C2 framework detector that scans files, scripts and configs for Cobalt Strike, Sliver, Mythic,… |
| [OCarve](https://github.com/owlsecx/OCarve) | File Carving Suite covering Binary , Disk Images , Memory Dumps , Network Captures; JPEG , PNG , PDF , ZIP , EXE . |
| [OCarveX](https://github.com/owlsecx/OCarveX) | File carving from binary streams — extract embedded files by magic signature, reconstruct fragmented data, generate. |
| [OCloud](https://github.com/owlsecx/OCloud) | Cloud Evidence Collector for authorized security testing and analysis. |
| [OCtopus](https://github.com/owlsecx/OCtopus) | Tactical Traffic Dissector & Credential Hunter covering Version : 1.0. |
| [ODeep](https://github.com/owlsecx/ODeep) | Digital forensics suite for carving, entropy, steganography, memory and timeline analysis. |
| [ODisk](https://github.com/owlsecx/ODisk) | ODisk — Advanced Low-Level Disk Forensic Suite for authorized security testing. |
| [OHex](https://github.com/owlsecx/OHex) | Professional Hex Editor & Binary Forensics Toolkit covering Version : 1.1.0. |
| [OIdsCfg](https://github.com/owlsecx/OIdsCfg) | IDS / NSM / HIDS Configuration Auditor for authorized security testing and analysis. |
| [OInbox](https://github.com/owlsecx/OInbox) | Parse raw email headers , SPF/DKIM/DMARC , Hop path , Spoofing detection , Risk scoring , GeoIP lookup , Lookalike. |
| [OLint](https://github.com/owlsecx/OLint) | Scan source code files for dangerous patterns, security vulnerabilities, and bad practices. |
| [OLogX](https://github.com/owlsecx/OLogX) | Security Log Analyzer / SIEM-lite for authorized security testing and analysis. |
| [OMem](https://github.com/owlsecx/OMem) | Professional live-memory forensics for Debian-based systems. RAM dump , process maps , string mining (ASCII +. |
| [ONetX](https://github.com/owlsecx/ONetX) | Network forensic and traffic analysis toolkit with Geo-IP, process mapping and live connections. |
| [OPcap](https://github.com/owlsecx/OPcap) | Offline PCAP Forensic Analyzer for authorized security testing and analysis. |
| [OPhish](https://github.com/owlsecx/OPhish) | Phishing & Smishing Detection Engine v1.0 covering owlsec.org , part of the O-toolkit; Debian Linux Edition —. |
| [OPhishGuard](https://github.com/owlsecx/OPhishGuard) | Phishing Email Analyzer for authorized security testing and analysis. |
| [OProc](https://github.com/owlsecx/OProc) | Process Behavioral & Memory Forensic Analyzer for authorized security testing and analysis. |
| [ORadar](https://github.com/owlsecx/ORadar) | Visualize RDP brute-force sources on an interactive map. |
| [ORaptor](https://github.com/owlsecx/ORaptor) | Identify , Partition , Carve , Hash , Strings , Report RAW / E01-header / VMDK / VDI / QCOW2 image analysis MBR/GPT. |
| [OReg](https://github.com/owlsecx/OReg) | Audit cron, systemd, init.d, rc.local, SSH, shell profiles, kernel modules, SUID/SGID, at jobs, XDG autostart. |
| [ORegHunt](https://github.com/owlsecx/ORegHunt) | Offline Windows Registry Hive Hunter for authorized security testing and analysis. |
| [ORisk](https://github.com/owlsecx/ORisk) | USB Guardian that scans, monitors, whitelists and quarantines USB devices for forensics. |
| [ORule](https://github.com/owlsecx/ORule) | Firewall Rule Change Auditor: Forensics-grade firewall monitoring & diffing. |
| [OScorer](https://github.com/owlsecx/OScorer) | PowerShell Obfuscation Scorer: Risk scoring for PowerShell obfuscation techniques. |
| [OSight](https://github.com/owlsecx/OSight) | Query live endpoint data using SQL. Collect process, port, user, file, network, and system intelligence for purple. |
| [OTele](https://github.com/owlsecx/OTele) | Authorized motion monitor for physical-security lab camera and motion detection. |
| [OUSBTrace](https://github.com/owlsecx/OUSBTrace) | Parse Windows registry hives for complete USB history USBSTOR , MountedDevices , Enum\USB , SetupAPI Anomaly. |
| [OVerifyX](https://github.com/owlsecx/OVerifyX) | Cryptographic hash calculation & verification, multi-algorithm, batch mode, deep file analysis, tamper detection. |
| [OVolatile](https://github.com/owlsecx/OVolatile) | Advanced memory forensics suite built on Volatility 3 with 55+ plugins and TUI. |
| [OWarning](https://github.com/owlsecx/OWarning) | Credential Dumping Early Warning: File + Process + ptrace/TracerPid correlation. |
| [OYaraX](https://github.com/owlsecx/OYaraX) | Signature & IOC Malware Scanner for authorized security testing and analysis. |

### Hardening/Defensive (57)

| Tool | Description |
| --- | --- |
| [OAMSIChk](https://github.com/owlsecx/OAMSIChk) | OAMSIChk is a defensive AMSI/ETW evasion detector that scans PowerShell scripts and files for AMSI bypasses, ETW… |
| [OAnon](https://github.com/owlsecx/OAnon) | Privacy and anonymity control center for Tor routing, leak checks and identity management. |
| [OAppArmor](https://github.com/owlsecx/OAppArmor) | Offline AppArmor Profile Auditor for authorized security testing and analysis. |
| [OAppArmorGen](https://github.com/owlsecx/OAppArmorGen) | OAppArmorGen is an AppArmor profile studio that generates profiles from templates or ELF binaries, lints existing… |
| [OAttackIQ](https://github.com/owlsecx/OAttackIQ) | Breach and Attack Simulation (BAS) Tool covering A lightweight tool to safely test security controls and improve. |
| [OAttckNav](https://github.com/owlsecx/OAttckNav) | OAttckNav is an offline MITRE ATT&CK navigator for searching 706 techniques and 174 threat groups, building… |
| [OAuditd](https://github.com/owlsecx/OAuditd) | Offline auditd Rules & Config Auditor for authorized security testing and analysis. |
| [OBackup](https://github.com/owlsecx/OBackup) | Offline Backup Configuration & Exposure Auditor for authorized security testing and analysis. |
| [Oblivion](https://github.com/owlsecx/Oblivion) | Real-time ransomware shield using filesystem monitoring, entropy, burst analysis and quarantine. |
| [OBootX](https://github.com/owlsecx/OBootX) | Linux Boot-Chain Security Auditor for authorized security testing and analysis. |
| [OCapAudit](https://github.com/owlsecx/OCapAudit) | Linux File Capabilities & SetUID Auditor for authorized security testing and analysis. |
| [OCaps](https://github.com/owlsecx/OCaps) | OCaps is a Linux capabilities auditor that decodes capability masks, audits processes and file capabilities, finds… |
| [OCassandraX](https://github.com/owlsecx/OCassandraX) | Offline NoSQL Wide-Column / Document Store for authorized security testing and analysis. |
| [OChain](https://github.com/owlsecx/OChain) | Propagation path discovery, MITRE ATT&CK coverage, credential exposure, lateral movement indicators, network. |
| [OCronAudit](https://github.com/owlsecx/OCronAudit) | Scheduled-Task & Persistence Auditor for authorized security testing and analysis. |
| [OCronGen](https://github.com/owlsecx/OCronGen) | OCronGen is a crontab studio that builds, explains and validates cron expressions, previews next runs, lints… |
| [OCupsX](https://github.com/owlsecx/OCupsX) | CUPS Printing-Service Configuration Auditor for authorized security testing and analysis. |
| [OCymulate](https://github.com/owlsecx/OCymulate) | Breach & Attack Simulation (BAS): Safe adversary simulation for detection testing. |
| [OElasticX](https://github.com/owlsecx/OElasticX) | Offline Elasticsearch / OpenSearch Config Auditor for authorized security testing and analysis. |
| [OEvade](https://github.com/owlsecx/OEvade) | Simulate evasion TECHNIQUE INDICATORS to validate EDR/XDR behavioural rules and blue-team detection. Distinct from. |
| [OFim](https://github.com/owlsecx/OFim) | Host File Integrity Monitor for authorized security testing and analysis. |
| [OFirewall](https://github.com/owlsecx/OFirewall) | Offline Firewall Ruleset Auditor for authorized security testing and analysis. |
| [OFlatSnap](https://github.com/owlsecx/OFlatSnap) | Flatpak & Snap Sandbox Permission Auditor for authorized security testing and analysis. |
| [OGrafanaX](https://github.com/owlsecx/OGrafanaX) | Observability-Stack Configuration Auditor for authorized security testing and analysis. |
| [OGraylogX](https://github.com/owlsecx/OGraylogX) | Graylog Server Configuration Hardening Auditor for authorized security testing and analysis. |
| [OHardn](https://github.com/owlsecx/OHardn) | Linux Host Hardening Auditor for authorized security testing and analysis. |
| [OIcingaX](https://github.com/owlsecx/OIcingaX) | Monitoring Configuration Hardening Auditor for authorized security testing and analysis. |
| [OKafkaX](https://github.com/owlsecx/OKafkaX) | Apache Kafka / ZooKeeper Configuration Auditor for authorized security testing and analysis. |
| [OLuksX](https://github.com/owlsecx/OLuksX) | Linux Disk-Encryption Configuration Auditor for authorized security testing and analysis. |
| [OMemcacheX](https://github.com/owlsecx/OMemcacheX) | Memcached & Varnish Cache Hardening Auditor for authorized security testing and analysis. |
| [OMongoX](https://github.com/owlsecx/OMongoX) | Offline MongoDB Configuration Auditor for authorized security testing and analysis. |
| [OMySqlX](https://github.com/owlsecx/OMySqlX) | MySQL / MariaDB Configuration Auditor for authorized security testing and analysis. |
| [OPgX](https://github.com/owlsecx/OPgX) | Offline PostgreSQL Configuration Auditor for authorized security testing and analysis. |
| [OPrivEsc](https://github.com/owlsecx/OPrivEsc) | Local Privilege Escalation Enumerator for authorized security testing and analysis. |
| [OPromX](https://github.com/owlsecx/OPromX) | Prometheus Monitoring-Stack Configuration Auditor for authorized security testing and analysis. |
| [ORabbitX](https://github.com/owlsecx/ORabbitX) | Offline RabbitMQ Configuration Auditor for authorized security testing and analysis. |
| [ORedisX](https://github.com/owlsecx/ORedisX) | Redis / Valkey / KeyDB Configuration Auditor for authorized security testing and analysis. |
| [OSbom](https://github.com/owlsecx/OSbom) | Software Bill of Materials & Advisories for authorized security testing and analysis. |
| [OSeccomp](https://github.com/owlsecx/OSeccomp) | Offline seccomp-bpf Profile Auditor for authorized security testing and analysis. |
| [OSeLinux](https://github.com/owlsecx/OSeLinux) | Offline SELinux Configuration & Policy for authorized security testing and analysis. |
| [OSharp](https://github.com/owlsecx/OSharp) | Purple Team Simulator: Safe adversary technique simulation (Linux). |
| [OShield](https://github.com/owlsecx/OShield) | Login behavior anomaly engine (UEBA) using temporal, geo, velocity and device signals. |
| [OSshAudit](https://github.com/owlsecx/OSshAudit) | SSH Configuration & Exposure Auditor for authorized security testing and analysis. |
| [OSupply](https://github.com/owlsecx/OSupply) | Software Supply-Chain Risk Auditor for authorized security testing and analysis. |
| [OSysctl](https://github.com/owlsecx/OSysctl) | Kernel sysctl Hardening Auditor for authorized security testing and analysis. |
| [OSyslogX](https://github.com/owlsecx/OSyslogX) | System Log Daemon Configuration Hardening Auditor for authorized security testing and analysis. |
| [OSystemdX](https://github.com/owlsecx/OSystemdX) | systemd Service Sandboxing & Exposure Scorer for authorized security testing and analysis. |
| [OThreat](https://github.com/owlsecx/OThreat) | Malicious URL Intelligence Engine: URL reputation via VirusTotal + URLScan.io. |
| [OTorX](https://github.com/owlsecx/OTorX) | Tor privacy suite for circuit control, browser routing, identity and DNS leak testing. |
| [OTrap](https://github.com/owlsecx/OTrap) | Emulate SSH , HTTP , FTP , Telnet , SMTP , MySQL Redis , RDP , DNS to detect, score, and store attacker activity. |
| [OUsbGuard](https://github.com/owlsecx/OUsbGuard) | USBGuard Policy & USB Authorization Auditor for authorized security testing and analysis. |
| [OVarnishX](https://github.com/owlsecx/OVarnishX) | Varnish Cache Configuration Hardening Auditor for authorized security testing and analysis. |
| [OVigilant](https://github.com/owlsecx/OVigilant) | Advanced system monitoring and security audit tool for Debian Linux hosts. |
| [OVpnAudit](https://github.com/owlsecx/OVpnAudit) | VPN Configuration Auditor for authorized security testing and analysis. |
| [OWardenX](https://github.com/owlsecx/OWardenX) | Vaultwarden Deployment Hardening Auditor for authorized security testing and analysis. |
| [OXrdpX](https://github.com/owlsecx/OXrdpX) | Remote-Desktop Server Configuration Auditor for authorized security testing and analysis. |
| [OZabbixX](https://github.com/owlsecx/OZabbixX) | Monitoring-Agent Configuration Auditor for authorized security testing and analysis. |

### Wireless/BLE (8)

| Tool | Description |
| --- | --- |
| [OArmor](https://github.com/owlsecx/OArmor) | Craft and transmit ARP Request / Reply / Gratuitous / Probe frames. Network ARP sweep, OUI vendor lookup, hex. |
| [OBeaconFlood](https://github.com/owlsecx/OBeaconFlood) | OBeaconFlood is a defensive Wi-Fi lab tool that detects rogue beacon and SSID-flood attacks (mdk3/mdk4-style) in… |
| [OBLE](https://github.com/owlsecx/OBLE) | Bluetooth / BLE Security Auditor for authorized security testing and analysis. |
| [OBLEScan](https://github.com/owlsecx/OBLEScan) | OBLEScan is a defensive Bluetooth Low Energy enumerator that parses BLE captures to identify advertising devices,… |
| [OBTClassic](https://github.com/owlsecx/OBTClassic) | OBTClassic is a defensive Bluetooth Classic (BR/EDR) recon analyzer that decodes device-discovery CSVs, classifying… |
| [OChanHop](https://github.com/owlsecx/OChanHop) | OChanHop is an offline Wi-Fi channel planner that analyzes site-survey CSVs, scores interference across 2.4/5/6 GHz… |
| [OMac](https://github.com/owlsecx/OMac) | Professional MAC Address Management Suite covering Version : 1.0.0. |
| [OWifiAudit](https://github.com/owlsecx/OWifiAudit) | Wi-Fi Security Auditor for authorized security testing and analysis. |

### Crypto (30)

| Tool | Description |
| --- | --- |
| [OAlchemy](https://github.com/owlsecx/OAlchemy) | Data Processor for authorized security testing and analysis. |
| [OAnalyze](https://github.com/owlsecx/OAnalyze) | Professional cryptanalysis toolkit for frequency analysis and classical cipher attacks. |
| [OASN1](https://github.com/owlsecx/OASN1) | OASN1 is an ASN.1/DER/X.509 lab that decodes and lints DER structures and inspects certificates, keys, CSRs and… |
| [OCertMonitor](https://github.com/owlsecx/OCertMonitor) | Certificate Transparency Monitor: Monitor CT logs for suspicious SSL/TLS certificates. |
| [OCertX](https://github.com/owlsecx/OCertX) | X.509 certificate inspector for TLS chains, expiry, fingerprints, OCSP and CSR analysis. |
| [OChecksum](https://github.com/owlsecx/OChecksum) | OChecksum is a file integrity lab that hashes files with 20 algorithms, creates and verifies sha256sum/SFV/JSON… |
| [OCipher](https://github.com/owlsecx/OCipher) | Classical Cipher Tool for authorized security testing and analysis. |
| [OClassic](https://github.com/owlsecx/OClassic) | OClassic — Professional Classical Cipher Suite for authorized security testing. |
| [OConvertX](https://github.com/owlsecx/OConvertX) | Advanced Data Encoder / Decoder Suite: Multi-format encoding, decoding, analysis & crypto. |
| [OCrack](https://github.com/owlsecx/OCrack) | Professional hash and password cracker with dictionary, brute, mask and rule attacks. |
| [OCrypt](https://github.com/owlsecx/OCrypt) | Modern encryption utility with PBKDF2-SHA256 key stretching and secure local key storage. |
| [OCryptScan](https://github.com/owlsecx/OCryptScan) | Weak-Cryptography Source Auditor for authorized security testing and analysis. |
| [OCryptSim](https://github.com/owlsecx/OCryptSim) | Safe, non-destructive ransomware chain emulation for EDR / XDR / SIEM detection testing and incident response drills. |
| [ODecipher](https://github.com/owlsecx/ODecipher) | Text Sleuth & Cryptanalysis Suite: Text analysis, pattern detection, cryptanalysis. |
| [ODiff](https://github.com/owlsecx/ODiff) | Compare hashes, keys, certs, binary files, encoded data. Highlight differences at byte / bit / char level.. |
| [OEncode](https://github.com/owlsecx/OEncode) | Multi-layer encode/decode pipelines for CTF & forensics Auto-detect , Recursive unwrap , XOR/Caesar brute. |
| [OEntropy](https://github.com/owlsecx/OEntropy) | Measure randomness quality of files, text, byte streams, and cryptographic keys. |
| [OForge](https://github.com/owlsecx/OForge) | Generate targeted wordlists from mask patterns. Custom charsets, rule engine, stats preview, multi-mask batch. |
| [OGpgX](https://github.com/owlsecx/OGpgX) | Offline GnuPG / OpenPGP Keyring Auditor for authorized security testing and analysis. |
| [OHashId](https://github.com/owlsecx/OHashId) | Hash Identifier & Cracker for authorized security testing and analysis. |
| [OJA3](https://github.com/owlsecx/OJA3) | OJA3 is a TLS fingerprinting lab that computes JA3, JA3S, JA4 and JA4S fingerprints from PCAPs, raw hellos or live… |
| [OKey](https://github.com/owlsecx/OKey) | Derive cryptographic keys from passwords using PBKDF2, scrypt, bcrypt*, Argon2*. Password strength meter, salt. |
| [OLicense](https://github.com/owlsecx/OLicense) | OLicense is a license and SPDX scanner that identifies licenses in source trees, validates SPDX expressions, checks… |
| [OPad](https://github.com/owlsecx/OPad) | Generate cryptographically secure OTP keys, encrypt and decrypt text/files using Vernam XOR cipher, key entropy. |
| [OPass](https://github.com/owlsecx/OPass) | Cryptographically secure password generation with strength scoring, passphrases, history & export. |
| [OPolicy](https://github.com/owlsecx/OPolicy) | Password Policy Auditor & Advisor for authorized security testing and analysis. |
| [OSignal](https://github.com/owlsecx/OSignal) | RSA & ECDSA digital signatures, key management, certificate inspection, and signature audit. |
| [OStrength](https://github.com/owlsecx/OStrength) | Professional Password Strength Analyzer. |
| [OTLSScan](https://github.com/owlsecx/OTLSScan) | TLS/SSL Configuration Auditor for authorized security testing and analysis. |
| [OVault](https://github.com/owlsecx/OVault) | Encrypted local password vault with full credential management and advanced security. |

### OSINT (11)

| Tool | Description |
| --- | --- |
| [OAlias](https://github.com/owlsecx/OAlias) | Generate highly realistic fake identities for authorised penetration testing, security awareness training, red team. |
| [ODigest](https://github.com/owlsecx/ODigest) | Deep text analysis , frequency , entropy , language detection , pattern extraction , readability , NLP scoring . |
| [ODigger](https://github.com/owlsecx/ODigger) | Username reconnaissance across 100+ platforms. Social / Tech / Gaming / Dev / Forum / Creative. Live tracking. |
| [OEmailHarvest](https://github.com/owlsecx/OEmailHarvest) | Gather emails and subdomains via OSINT: crt.sh, HackerTarget, AlienVault OTX, BufferOver, ThreatCrowd, RapidDNS. |
| [OIndex](https://github.com/owlsecx/OIndex) | Build, organise and run Google dork queries. 100+ built-in templates across 14 categories. Interactive dork. |
| [OPassport](https://github.com/owlsecx/OPassport) | Advanced IP/Domain geolocation with multi-API fallback, WHOIS lookup, threat intelligence, DNS records, port scan. |
| [OSubStorm](https://github.com/owlsecx/OSubStorm) | OSubStorm — Subdomain & DNS Intelligence Harvester for authorized security testing. |
| [OTaker](https://github.com/owlsecx/OTaker) | Subdomain Asset Visualizer: Screenshots , HTML Report , ASN , Wayback , CVE. |
| [Ouser](https://github.com/owlsecx/Ouser) | OSINT Username Scanner: Multi-platform username presence detection. |
| [OWayback](https://github.com/owlsecx/OWayback) | Wayback Machine archive scanner for historical URL and subdomain recon. |
| [OWordlist](https://github.com/owlsecx/OWordlist) | Advanced OSINT-based wordlist generator for Debian Linux. |

### CTF (4)

| Tool | Description |
| --- | --- |
| [OBaseConv](https://github.com/owlsecx/OBaseConv) | OBaseConv is a base converter and encoding lab that converts numbers between bases 2–62, encodes and decodes 24… |
| [OCSVLab](https://github.com/owlsecx/OCSVLab) | OCSVLab is a CSV/TSV data lab for previewing, filtering, sorting, deduplicating, profiling and converting tabular… |
| [OCTF](https://github.com/owlsecx/OCTF) | CTF Swiss Knife Tool for authorized security testing and analysis. |
| [OSteg](https://github.com/owlsecx/OSteg) | Professional Steganography Suite for authorized security testing and analysis. |

### Utilities (6)

| Tool | Description |
| --- | --- |
| [OChronyX](https://github.com/owlsecx/OChronyX) | Time-Synchronization Config Auditor for authorized security testing and analysis. |
| [OMail](https://github.com/owlsecx/OMail) | Professional-grade authorised phishing simulation & security awareness testing platform. |
| [ONotes](https://github.com/owlsecx/ONotes) | Encrypted Operator Notebook for authorized security testing and analysis. |
| [OParse](https://github.com/owlsecx/OParse) | Format , Validate , Convert , Diff , Schema , Query JSON ↔ XML ↔ YAML ↔ TOML ↔ CSV JMESPath query , JSONSchema. |
| [OReport](https://github.com/owlsecx/OReport) | Pentest Report & Findings Generator for authorized security testing and analysis. |
| [OSupport](https://github.com/owlsecx/OSupport) | Incident and system reporting tool for collecting diagnostics and support packages. |

---

## Legal / Responsible use

> ⚠️ **AUTHORISED USE ONLY** — Owl OS and every tool in this repository are for authorised security testing, research and defensive operations on systems you own or have explicit written permission to assess. Unauthorised access, surveillance or misuse is illegal.

---

## Contact

- Website: [https://owlsec.org](https://owlsec.org)
- Email: support@owlsec.org
- WhatsApp: [Owl OS channel](https://whatsapp.com/channel/0029VbCOxBDKwqSNPAJTrF44)

---

## ©️ License

MIT License — © Khaled S. Haddad
