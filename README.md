# 📊 Splunk SIEM Home Lab

## Project Overview

This project documents the configuration and use of Splunk as a Security Information and Event Management (SIEM) platform.

The lab focuses on collecting Windows security telemetry, monitoring system activity, investigating authentication events, detecting process activity, and building an incident timeline.

The goal of this project was to simulate a basic Security Operations Center (SOC) investigation workflow.

---

## Lab Environment

- Splunk SIEM
- Windows 11
- Windows Security Event Logs
- Windows Audit Policies
- PowerShell
- Virtualized Home Lab Environment

---

# SOC Investigation Workflow

## 1. Configuring Windows Audit Policies

![Splunk Audit Policy Configuration](Splunk%201%20audit%20policy%20config.png)

Configured Windows audit policies to generate security telemetry that could be collected and analyzed by Splunk.

Audit policy configuration is an important first step in security monitoring because a SIEM can only analyze events that are being properly generated and logged.

---

## 2. Enabling Process Creation Logging

![Process Creation Logging](Splunk%202%20Process%20creation.png)

Configured process creation auditing to monitor when new processes are launched on the Windows system.

Process creation events can provide valuable information during investigations by showing which programs were executed and when they were launched.

---

## 3. Receiving Windows Events in Splunk

![Receiving Windows Events](Splunk%203%20Receiving%20windows%20events.png)

Verified that Windows event data was successfully being received and indexed by Splunk.

This demonstrates the log collection stage of the SIEM workflow, where endpoint telemetry is centralized for searching and investigation.

### Additional Event Data

![Additional Windows Events](Splunk%203%20Receiving%20windows%20events%20pt.2.png)

Reviewed additional Windows event data being received by Splunk to verify that the logging pipeline was functioning correctly.

---

## 4. Investigating Account Creation

![Account Creation Event](Splunk%204%20acct%20creation%20event.png)

Investigated account creation activity within the Windows event logs.

Monitoring account creation is important because unauthorized accounts can potentially be used to maintain persistence or gain access to systems.

---

## 5. Investigating Failed Authentication

![Failed Login Investigation](Splunk%204%20creating%20a%20failed%20login.png)

Generated and investigated a failed login event to simulate suspicious authentication activity.

Failed authentication attempts can be indicators of password guessing, brute-force activity, or user authentication errors. The event must be analyzed in context to determine whether the activity is suspicious.

---

## 6. Investigating Process Creation Events

![Process Creation Event](Splunk%204%20process%20creation%20evt.png)

Reviewed process creation events collected from the Windows system.

Process monitoring allows analysts to investigate what programs were executed and can help identify potentially suspicious or unexpected activity.

### Additional Process Event Analysis

![Additional Process Creation Event](Splunk%204%20process%20creation%20evt%20pt.2.png)

Performed additional analysis of process creation telemetry to examine the available event information during an investigation.

---

## 7. PowerShell Process Detection

![PowerShell Process Detection](Splunk%205%20powershell-process-detection.png)

Created a detection focused on PowerShell process activity.

PowerShell is a legitimate Windows administration tool, but it is also commonly monitored by security teams because attackers may abuse it to execute commands, automate activity, or perform post-compromise actions.

Monitoring PowerShell execution provides valuable visibility during endpoint investigations.

---

# 8. SOC Dashboard

![Splunk SOC Dashboard](Splunk%206%20splunk-soc-dashboard.png)

Created a SOC-focused dashboard to provide a centralized view of security-related activity.

Dashboards can help analysts quickly identify trends, investigate events, and monitor important security telemetry from a single location.

---

# 9. Building an Investigation Timeline

![Investigation Timeline](Splunk%207%20building%20a%20timeline.png)

Built an investigation timeline to organize security events chronologically.

Creating a timeline helps analysts understand the sequence of activity and determine how individual events may be related.

### Additional Timeline Analysis

![Timeline Analysis](Splunk%207%20building%20a%20timeline%20pt.2.png)

Continued analyzing the event timeline to correlate activity and better understand the progression of the investigation.

---

# 10. Incident Investigation

![Incident Investigation](Splunk%207%20incident-passwordreset-logins.png)

Investigated password reset and authentication-related activity using Splunk.

This investigation demonstrates how multiple events can be reviewed together to identify relationships between authentication activity and account changes.

A timeline-based approach helps an analyst determine whether activity appears normal or requires additional investigation.

---

# Investigation Summary

During this project, I configured and used Splunk to analyze Windows security telemetry and simulate a basic SOC investigation.

The investigation included:

- Configuring Windows audit policies
- Monitoring process creation
- Receiving Windows event data in Splunk
- Investigating account creation events
- Analyzing failed authentication attempts
- Detecting PowerShell process activity
- Building a SOC dashboard
- Creating an investigation timeline
- Reviewing password reset and authentication activity

This project demonstrates a basic SIEM workflow used in Security Operations Center environments:

> **Generate telemetry → Collect logs → Search events → Detect suspicious activity → Correlate events → Investigate the incident**

---

# Learning Outcomes

Through this project I developed practical experience with:

- SIEM fundamentals
- Splunk log ingestion
- Splunk search and analysis
- Windows audit policies
- Windows Security Event Logs
- Process creation monitoring
- PowerShell activity monitoring
- Authentication monitoring
- Account activity investigation
- Security event correlation
- SOC dashboards
- Incident timelines
- Basic detection and investigation workflows
