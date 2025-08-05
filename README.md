# incident-response-automation
Simulates a full incident response lifecycle with automated detection, alerting, and reporting in a SOC environment.


---

## Incident Response Simulation with Automation  
**Author:** Niharika Kalkeri  
**Tools:** Windows/Linux VMs, PowerShell, Invoke-Mimikatz, Splunk/ELK, Python, Bash  

---

### Project Summary

Fast and effective incident response is critical to minimizing damage from attacks like phishing, malware execution, or insider data theft. This project simulates a realistic incident scenario in a lab environment, covering:

- Attack simulation (e.g., phishing leading to malware and C2 beaconing)  
- Log ingestion into SIEM tools (Splunk or ELK)  
- Custom detection rules for suspicious activity  
- Automation scripts to generate alerts, reports, and simulate remediation  

The project models real SOC workflows and demonstrates the value of automation in reducing response time.

---

### Real-World Problem

Organizations often struggle to:  

- Detect malicious activity quickly from noisy logs  
- Create accurate detection rules for complex attack behaviors  
- Automate alerting and remediation to prevent escalation  
- Provide clear incident reports for decision makers  

---

### What This Project Does

- Simulates attacks generating relevant logs (PowerShell, network, host activity)  
- Ingests logs into Splunk or ELK Stack  
- Detects suspicious events with custom queries/rules  
- Flags risky actions like unusual PowerShell commands, privilege escalations, or suspicious network connections  
- Automates alert generation and reporting (CSV, PDF)  
- Simulates response actions like account disabling or host isolation  



---

### Key Components

| Component        | Description                                         |
|------------------|-----------------------------------------------------|
| Attack Simulation| Invoke-Mimikatz, PowerShell scripts, synthetic logs |
| Log Ingestion    | Splunk or ELK configured to collect Windows/Linux logs |
| Detection Rules  | Custom searches detecting malicious behavior        |
| Automation       | Python/Bash scripts to alert and simulate response  |
| Reporting        | Incident timeline and detailed analyst report       |

---

### Sample Detection Query Example (Splunk)

```splunk
index=wineventlog EventCode=4104 | search CommandLine="*encodedcommand*"

---

## 🔎 Example Attacker Behavior This Catches

- Phishing leading to malware execution and C2 beaconing  
- Insider threat data exfiltration via email  
- Suspicious PowerShell command execution  
- Privilege escalation and unusual logins  

---

## 🧠 Lessons Learned

- Simulating realistic incidents helps understand attacker behaviors  
- Timely log ingestion and monitoring is vital  
- Custom detection rules improve alert accuracy  
- Automation streamlines SOC response and reduces time to containment  

---

## 🚀 How to Run This Locally

### 1. Set Up Lab Environment

- Configure Windows and Linux VMs  
- Deploy Splunk or ELK for log ingestion  
- Prepare simulated attack scripts or log files  

### 2. Install Requirements

```bash
pip install splunk-sdk pandas reportlab

### 3. Run Automation Scripts
```bash
python incident_response_automation.py



📚 References
MITRE ATT&CK Framework

NIST SP 800-61 Incident Handling Guide

Splunk Documentation

Invoke-Mimikatz GitHub

PowerShell Security Best Practices

🧑‍💻 Author
Niharika Kalkeri
Aspiring Cybersecurity Analyst | Security+ | AWS | Python
