# 🛡️ Weekend SOC Lab Project: Detection, Alerting, and Automated Response

## 🚨 Overview

This weekend, I built a mini SOC (Security Operations Center) lab to simulate and respond to real-world attack scenarios. The project focuses on **detection**, **alerting**, and **automated incident response** — a practical exercise for enhancing blue team skills.

---

## 🔧 Lab Setup

- ✅ **Active Directory Domain Controller** (On-Prem)
- ✅ **Windows Machine** (Simulated Compromised Endpoint)
- ✅ **SOC Analyst Workstation**
- ✅ **Splunk** (on Ubuntu) for log collection and detection
- ✅ **Slack** for real-time alert notifications
- ✅ **Shuffle SOAR** for automated incident response playbooks

---

## 🎯 Attack Scenario

1. An attacker gains access to the Windows machine.
2. **Splunk** detects the suspicious activity and sends an alert to **Slack**.
3. **Shuffle** triggers a SOAR playbook that:
   - Sends an **email notification** to the SOC analyst.
   - Asks for approval to **disable the compromised user account**.

---

## 💡 Why This Matters

This lab replicates the core components of a real-life SOC environment, integrating:
- Threat detection
- Alerting mechanisms
- Automated response with human-in-the-loop decision-making

Ideal for:
- Practicing **incident response**
- Learning **SIEM/SOAR integration**
- Building hands-on **blue team** experience

---

## 📬 Let's Connect

If you're working on your own SOC lab, interested in collaboration, or have feedback, feel free to **connect or reach out**!

---

## 📢 Follow the Project Series

I'll be sharing step-by-step content throughout the week on different platforms:

- 🔗 **LinkedIn** – Project highlights and updates  
- 📺 **YouTube** – Lab setup, detections, and attack simulation  
- 💻 **GitHub** – Scripts, configurations, and SOAR playbooks *(you’re here!)*  
- ✍️ **Medium** – Deep technical walkthroughs and tutorials

---

## 📂 Coming Soon to This Repo

- [ ] PowerShell scripts for simulation
- [ ] Splunk detection rules
- [ ] SOAR playbook templates (Shuffle)
- [ ] Slack + email alerting integration guide

Stay tuned!
