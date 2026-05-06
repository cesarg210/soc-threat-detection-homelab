# 🚨 Password Spraying Detection

## 📌 Overview

Password spraying is a technique where an attacker attempts a single password across multiple user accounts to avoid account lockouts and detection.

---

## ⚔️ Attack Simulation

### Attacker Machine:

Kali Linux

### Tool Used:

NetExec (nxc)
#### File used for attack (executes multiple usernames of windows client)
![Spray attack setup](../screenshots/password-spray-attack-setup.png)

## 🛡️ Detection Rule (Kibana)
![Spray attack rule](../screenshots/Password-spraying-rule-creation.png)
### Attack Pattern:

* Same source IP
* Multiple usernames
* Same password
* Single attempt per user

---

## 🔍 Detection Logic

The rule identifies:

* A single source IP attempting logins
* Across multiple user accounts
* Within a short time window

This behavior is indicative of password spraying.

---

## 📸 Evidence

![spray attack](../screenshots/password-spray-attack.png)
![spray attack](../screenshots/source-ip-detected.png)
* Kali attack execution
* Kibana logs (Discover view)
* Alert generated in Security → Alerts

