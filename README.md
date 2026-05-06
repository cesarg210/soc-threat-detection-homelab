# 🔴 Threat Detection & Attack Simulation

## 📌 Overview

This lab focuses on building both offensive and defensive skills by generating controlled attacks from a Kali Linux machine and detecting them through custom detection rules in Kibana.

---

### Focus Areas:

* Controlled attack simulations using Kali Linux
* Brute force and password spraying attacks
* Indicator of Compromise (IOC) identification
* Detection engineering using Elastic SIEM VM
* Alert validation and tuning
* Documentation of detection workflows

---

## 🏗️ Lab Architecture

* **SIEM:** Elastic Stack (Elasticsearch + Kibana + Fleet)
* **Endpoint Monitoring:** Elastic Agent
* **Attacker Machine:** Kali Linux
* **Target Systems:**

  * Windows 11 Client (Domain-joined)
  * Linux Domain Controller (Samba AD)

---

## ⚔️ Attacks Simulated

| Attack Type                    | Description                                         |
| ------------------------------ | --------------------------------------------------- |
| Port Scanning                  | Network reconnaissance using Nmap                   |
| Brute Force                    | Multiple password attempts against a single account |
| Password Spraying              | Single password attempt across multiple accounts    |
| Successful Login After Failure | Credential compromise simulation                    |

---

## 🛡️ Detection Capabilities

Custom detection rules were created in Kibana to identify:

* Repeated failed login attempts (Event ID 4625)
* Password spraying behavior using user cardinality
* Successful logins following failed attempts (Event ID 4624)
* Source IP correlation for attacker identification

---

## 🚀 Skills Demonstrated

* SIEM deployment and configuration
* Endpoint telemetry ingestion
* Detection rule engineering
* Attack simulation using Kali Linux
* Log analysis and correlation
* Incident detection workflows
