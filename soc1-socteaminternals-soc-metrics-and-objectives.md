
## SOC Metrics and Objectives

<b>Difficulty: Easy</b> 

<b>Date Completed: 23/07/2026</b>  

<b>What did I learn:</b> 

- The concepts of SLA, MTTD, MTTA, and MTTR
  
- Understood the importance of the False Positive rate

- Practice managing SOC team performance metrics

<b>Prerequisites</b> 

- SOC Workbooks and Lookups room

<b>Tools</b> 

- THM Workbook Practice Site

## Process 

<b>Task 1: Introduction </b> 

This room is about exploring the "most common evaluation approaches like MTTD and MTTR, and describes both methods to improve the metrics and potential consequences of ignoring them" (THM, n.d.).

<b>Task 2: Core Metrics </b> 

The main goal of a SOC is to protect an organisation's digital assets by adhering to the CIA triad (Confidentiality , Integrity, and Availability).  

There are four kinds of metrics that a SOC should consider to protect the CIA of an organisation's digital assets:

| Metric | Formula | Measures |
| --- | --- | --- |
| Alerts Count | AC = Total Count of Alerts Recieved | Overall load of SOC analysts |
| False Positive Rate | FPR = Flase Positives / Total Alerts | Level of noise in the alerts |
| Alert Escalation Rate | AER = Escalated Alerts / Total Alerts | Experience of L1 analysts |
| Threat Detection Rate | TDR = Detected Threats / Total Threats | Reliability of the SOC team |

<b>Alerts Count</b> 

All the alerts including the noise. A lot of alerts may be overwhelming but a low count may indicate an issue within the SIEM, like lack of visibility. This could lead to undetected breaches. Around 5 to 30 alerts per day per L1 analyst is an ideal range. 

<b>False Positive Rate</b> 

If a majority of alerts are a false positive. This means that there is a lot of noise within the SIEM's detection. It should be as low as possible. False Positive alerts can usually be fixed using tools and detection rules tuning. This is so that there is less noise to sift through. 

<b>Alert Escalation Rate</b> 

The alert escalation rate metric evaluates how experienced and independent L1 analysts are, and how often they decide to escalate the alert. 
