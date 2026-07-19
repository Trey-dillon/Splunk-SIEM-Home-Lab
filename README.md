# 📊 Splunk SIEM Home Lab

## 🎯 Project Overview

This project documents the implementation of a Splunk SIEM home lab used to collect, monitor, and investigate Windows security events.

The project simulates a basic Security Operations Center (SOC) workflow by collecting Windows telemetry, monitoring process and authentication activity, and building an investigation timeline from security events.

### Skills Demonstrated

- SIEM fundamentals
- Splunk log ingestion
- Windows Event Log analysis
- Audit policy configuration
- Process creation monitoring
- Authentication monitoring
- PowerShell detection
- Incident timeline development
- Security event investigation

---

# 🛠️ Lab Environment

- Splunk SIEM
- Windows 11
- Windows Security Event Logs
- Windows Audit Policies
- PowerShell
- Virtualized home lab environment

---

# 🔍 Investigation Walkthrough

## 1. Configuring Windows Audit Policies

![Windows Audit Policy Configuration](screenshots/Splunk%201%20audit%20policy%20config.png)

Configured Windows audit policies to generate security telemetry for important system and user activity.

Audit policy configuration is an important first step in security monitoring because the SIEM can only analyze events that are being generated and collected.

---

## 2. Enabling Process Creation Auditing

![Process Creation Configuration](Splunk%202%20Process%20creation.png)

Configured process creation auditing to monitor when new processes are launched on the Windows system.

Monitoring process creation provides visibility into potentially suspicious activity, including the execution of scripts, administrative tools, and other processes.

---

## 3. Receiving Windows Events in Splunk

![Receiving Windows Events](Splunk%203%20Receiving%20windows%20events.png)

Verified that Windows event data was being received and indexed by Splunk.

Centralizing Windows telemetry in a SIEM allows analysts to search and investigate security activity from a single platform.

![Receiving Windows Events Part 2](Splunk%203%20Receiving%20windows%20events%20pt.2.png)

Confirmed additional Windows event data was being successfully received and processed by Splunk.

---

## 4. Investigating Account Creation Activity

![Account Creation Event](Splunk%204%20acct%20creation%20event.png)

Investigated a Windows account creation event within Splunk.

Monitoring account creation is important because unauthorized accounts can potentially be used to maintain persistence or gain access to systems.

---

## 5. Generating and Investigating a Failed Login

![Failed Login](Splunk%204%20creating%20a%20failed%20login.png)

Generated a failed authentication event to simulate suspicious login activity.

Failed authentication attempts can be important indicators during a security investigation, particularly when multiple failures occur within a short period of time.

---

## 6. Investigating Process Creation Events

![Process Creation Event](Splunk%204%20process%20creation%20evt.png)

Investigated process creation events collected from the Windows system.

Process creation logs provide visibility into programs and commands executed on a system and can assist analysts in identifying suspicious activity.

![Process Creation Event Part 2](Splunk%204%20process%20creation%20evt%20pt.2.png)

Reviewed additional process creation event data to further analyze the activity recorded by Windows.

---

## 7. PowerShell Process Detection

![PowerShell Process Detection](Splunk%205%20powershell-process-detection.png)

Created a Splunk search to identify PowerShell process activity.

PowerShell is a legitimate administrative tool but is also frequently monitored by security teams because it can be used to execute scripts and perform administrative actions.

Monitoring PowerShell activity helps analysts identify potentially suspicious command execution.

---

## 8. Building a SOC Dashboard

![SOC Dashboard](Splunk%206%20splunk-soc-dashboard.png)

Created a security monitoring dashboard to provide a centralized view of important activity observed in the lab environment.

Dashboards can help analysts quickly identify trends and prioritize events for further investigation.

---

## 9. Building an Investigation Timeline

![Investigation Timeline](Splunk%207%20building%20a%20timeline.png)

Built an investigation timeline by organizing security events in chronological order.

A timeline allows an analyst to understand how events occurred over time and helps connect related activities during an investigation.

![Investigation Timeline Part 2](Splunk%207%20building%20a%20timeline%20pt.2.png)

Expanded the timeline to correlate additional events and better understand the sequence of activity.

---

## 10. Incident Timeline and Investigation

![Incident Timeline](Splunk%207%20incident-passwrodreset-logins.png)

Created an incident timeline involving password reset activity and subsequent login events.

Organizing events chronologically helps establish a sequence of activity and provides context for determining whether behavior is normal or potentially suspicious.

---

# 🔎 Investigation Summary

During this project, I configured Windows auditing and used Splunk to collect, search, and investigate security telemetry.

The investigation included:

- Configuring Windows audit policies
- Monitoring process creation
- Collecting Windows events in Splunk
- Investigating account creation
- Generating and analyzing failed login activity
- Monitoring PowerShell execution
- Building a SOC dashboard
- Creating an incident timeline

This project demonstrates a basic SIEM workflow used in Security Operations Center environments: generating security telemetry, collecting logs, searching events, correlating activity, and investigating potentially suspicious behavior.

---

# 📖 Learning Outcomes

Through this project I developed practical experience with:

- Splunk SIEM
- Windows event collection
- Windows audit policies
- Process monitoring
- Authentication monitoring
- PowerShell detection
- Security event investigation
- Timeline analysis
- SOC dashboards
- Basic incident response workflows
