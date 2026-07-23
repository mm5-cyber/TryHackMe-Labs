
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

There are four kinds of metrics that should be considered to protect the CIA of an organisation's digital assets:

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

The alert escalation rate metric evaluates how experienced and independent L1 analysts are, and how often they decide to escalate the alert. An good range is anything below 50%, though companies should aim to have it below 20%. 

<b>Threat Detection Rate</b> 

The threat detection rate should always be at 100%, as any singular missed threat can be extremely problematic to a company. Terrible issues could arise like data exfiltration and ransomware. 

<b>Task 3: Triage Metrics</b> 

A Service Level Agreement is a document that is signed between the company management and the internal SOC. Or in a Managed Security Service (MSSP), it is signed between the SOC provider and its customers. Within the SLA, the agreement usually requires how quick threats should be detected. This is measured through Mean Time to Detect (MTTD). Then how quick the alert should be acknowledged / start triage of the alert. This is measured using Mean Time to Acknowledge (MTTA). Finally, responding to the threat to stop a breach from spreading. Which is measured through the Mean Time to Respond (MTTR) metric. 

Here is a timeline provided by TryHackMe on what the flow should look like: 

<img width="950" height="300" alt="image" src="https://github.com/user-attachments/assets/b5baa498-897e-480a-b275-178fbe589187" />

<sub>Thrreat Detection to Threat Response timeline. Notice how the MTTA is included in the MTTR time (THM, n.d.)</sub>

Here is a reference table also provided by THM, regarding the SOC metrics for a SLA: 

| Metric | Common SLA | Description |
| --- | --- | --- |
| SOC Team Availability | 24/7 | Working schedule of the SOC team, often Monday-Friday (8/5) or 24/7 mode |
| Mean Time to Detect (MTTD) | 5 minutes| Average time between the attack and its detection by SOC tools |
| Mean Time to Acknowledge (MTTA) | 10 minutes | Average time for L1 analysts to start triage of the new alert |
| Mean Time to Respond (MTTR) | 60 minutes | Average time taken by SOC to actualy stop the breach from spreading |






