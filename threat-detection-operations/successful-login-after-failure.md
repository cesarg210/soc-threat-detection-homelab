# 🔓 Successful Login After Failed Attempts Detection

## 📌 Overview

This detection identifies a potential account compromise where multiple failed login attempts are followed by a successful login.

---

## ⚔️ Attack Simulation
![execution](../screenshots/crackmapexecution.png)

---

## 🛡️ Detection Rule (EQL)
![Detection rule](../screenshots/successful-attempt-rule-creation.png)

---

## 🔍 Detection Logic

The rule detects:

* Multiple failed login attempts
* Followed by a successful login
* For the same user within a short time window

---

## 📸 Evidence
![Alert](../screenshots/successful-login-after-failure-alert.png)
* Failed login attempts in Discover
* Successful login event
* Alert generated in Kibana

