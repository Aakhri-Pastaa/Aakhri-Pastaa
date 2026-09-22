# Kunal Patil

First-year student on the **EIT Digital Master's in Cybersecurity (CSES)**, University of Twente (NL), exiting at University of Turku (FI) with a specialisation in Security Technologies and Intelligence. 120 ECTS across two EU universities.

Based in Enschede. Blue-team focused: detection engineering, security operations, and the infrastructure underneath both. Heading toward security consulting, and over time security or cloud architecture.

**Open to:** full-time summer internship, June to August 2027 · part-time work during term (16 hrs/week)

---

## Experience

**IT Operations & Cybersecurity Intern**, Delta System, India (remote) · Jul 2025 to Jan 2026

Sole security and IT function at a web, app and UI/UX design agency:

- Wazuh SIEM monitoring and incident response across 10+ endpoints serving 7+ client environments, triaging 500 to 1,000 alerts per week through Jira
- Rewrote correlation rules and active-response configuration, cutting false positives by 70%
- End-to-end Wazuh onboarding: agent deployment, log pipeline setup, VirusTotal integration, automated response to SSH and FTP brute-force attacks
- Administered and hardened 5 Linux servers to a secure configuration baseline
- Internal penetration testing and OWASP Top 10 assessments of client sites, with written remediation guidance for developers
- Monthly security reports covering events handled, actions taken and outcomes

First time running security tooling in a live environment rather than a lab, and the first time I learned that undocumented work is work nobody can verify.

---

## What I'm building

**Detection engineering lab, active**
Wazuh, Sigma rules, Atomic Red Team, n8n alert automation. Detection-as-code on a hardened Proxmox host. Every rule maps to a MITRE ATT&CK technique. Every alert has a runbook.

**Infrastructure foundation, done**
Self-hosted Proxmox stack: Vaultwarden, Linkwarden, Caddy reverse proxy with automated TLS via Let's Encrypt DNS-01. Zero public ports, Tailscale-gated. All services on `javaphile.org`, running on hardware I built myself.

**Next**
DevSecOps pipeline (Trivy, SBOM, Cosign, Semgrep) → Cloud CSPM (Prowler, Steampipe) → Kubernetes security (Falco, OPA) → LLM red-teaming (Garak, PyRIT). AZ-500 in progress.

---

## Projects

### [active-directory-wazuh-homelab](https://github.com/Aakhri-Pastaa/active-directory-wazuh-homelab)
Built twice. First fully on-prem on VMware Workstation: Windows Server domain controller, Linux VMs, virtual networking and snapshots, all on one laptop. Then again as a hybrid environment joined to Entra ID.

Running on top: Wazuh SIEM with Sysmon telemetry and custom detection rules, Suricata for network correlation, agentless log forwarding over SSH/SCP, and VirusTotal enrichment through Wazuh active response.

Extended it with a SOAR pipeline using **TheHive and Shuffle**, enriching Sysmon-sourced file hashes via the VirusTotal API to triage known-malicious execution automatically. I wanted to find out where automation stops being safe to trust.

### [kshieldvpn](https://github.com/Aakhri-Pastaa/kshieldvpn)
BSc dissertation project. Windows VPN client in C# and .NET with an OpenVPN backend, SQL Server credential store, Stripe billing and an AWS-hosted VPN server. Documented in a 99-page formal report.

### [ShadowTwin](https://github.com/Aakhri-Pastaa/ShadowTwin)
Security telemetry pipeline in Python: Wazuh alerts from rotating log files into Apache Kafka at-least-once, then into PostgreSQL exactly once — verified under crashes, broker and database outages, and log rotation while the forwarder is down. The forwarder runs on my homelab; the demo built to prove the guarantee found a data-loss bug in my own released v1.0.0, which I fixed and documented in v1.1.0.

### [Obsidian-Multi-Device-Sync-via-GitHub](https://github.com/Aakhri-Pastaa/Obsidian-Multi-Device-Sync-via-GitHub)
Free alternative to Obsidian Sync across laptops and Android through a private GitHub repository, with full version history and no subscription.

### API security testing, FastAPI
Tested a FastAPI service against common REST API weaknesses: broken authentication and authorisation, excessive data exposure, input validation gaps. Following APIsec University's API security course.

---

## Teaching

**Kerberos authentication**, group workshop, January 2024. Led a small group explaining how Kerberos works to an audience meeting it for the first time: the concept in plain terms, then a component-by-component breakdown, then an enactment of the full ticket exchange. Placed 2nd in the cohort. The enactment did more work than the explanation.

---

## Stack

**Security:** Wazuh · Sigma · Sysmon · Suricata · TheHive · Shuffle · Atomic Red Team · MITRE ATT&CK · CIS Benchmarks · Burp Suite · OWASP ZAP
**Cloud:** Azure · AWS · Entra ID / IAM
**Infrastructure:** Proxmox · VMware Workstation · Docker · Tailscale · Caddy · Ubuntu · Windows Server · Active Directory
**DevSecOps:** Trivy · Semgrep · Cosign · GitHub Actions (building)
**Dev:** C# · .NET · Python · Bash · Git · Jira

---

## Certifications

Ethical Hacking Essentials (EHE), EC-Council · Google Cybersecurity Professional Certificate · Splunk Search Expert
In progress: **AZ-500** · Planned: Security+, BTL1

---

[LinkedIn](https://linkedin.com/in/kunal-patil-0b4713276) · kunal.eu2026@gmail.com
