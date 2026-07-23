
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

<sub>SOC metrics reference table (THM, n.d.)</sub> 

<b>Task 4: Improving Metrics</b> 

Metrics were built to make the SOC more efficient, leading to making attacks far less successful. Metrics are also used to evaluate your own performance. 

TryHackMe provides reccomendations to resolve issues regarding SOC Metrics: 

- Falso Positive Rate over 80%: It means that your team recieves too much noise in their alerts. To remediate this try to exclude trusted activities like system updates from your EDR or SIEM detection rules and Consider automating alert triage for the most common alerts by using Security, Orchestration, Automation, and Response (SOAR), or have custom scripts written. 

- If the Mean Time to Detect (MTTD) is over 30 minutes, it means that there is a high delay in threat detection. To remediate this issue, consider contacting SOC engineers to make the detection rules run faster or with a higher rate. Also check if the SIEM logs are being collected in real-time, without delay. 

- If the Mean Time to Acknowledge is over 30 minutes, this means that there is a also a high delay when it comes to L1 analysts starting their alert triage. It's best to ensure that all analysts are being notified in real-time whenever a new alert appears. Also ensure that the alerts in the queue are being evenly distributed between the analysts that are on shift. This is so that no one analyst is being overloaded with work, resulting in a higher time to acknowledge the alert. 

- If the Mean Time to Respons (MTTR) is over 4 hours, this means that the SOC team cannot stop the breach in time. For L1 Analysts, they should priotise making everything possible to quickly escalate the threats to L2. Additionally, make sure that the team has documentaion on varioud different attack scenarios, so that these issues can be remediated effectively in a more timely manner. 

<b>Task 5: Practice Scenarios </b>  

In the practical lab for this room, you are put in the position of a SOC manager that is currently recieving three different complaints related to the SOC team. The goal is to correctly idenify the problematic metric involved, identify the task needed to improve this metric, and assign the task to the right person/people. 


The First Complaint: 

"Dear SOC manager, our biggest customer, OpenDoor Inc., was dissatisfied with how we handle breaches. When their CFO’s email and Entra ID account were breached, it took us almost 6 hours to kick out the hacker from the mailbox, and threat actors had enough time to dump all emails and leak them on Darknet. Looking at the report, looks like we had a critical alert and spent 5 hours trying to properly reset the victim’s Entra ID password and MFA. How could it happen, and what would be your actions?" 

Problematic Metric: 

The Time to respond was to high, too much time to spend to contain the attack.  

Improvement Task: 

Create a workbook explaining credential rotation steps, and present it to the team. This is a great task, as it will help the team be able to quickly and effectively resolve the issue. 

Assign Task To: 

Assign the research and workbook creation task to the L2 that handled the incident. 

The Second Complaint: 

"Hey, thanks for the SOC demo for our top management. They loved your ransomware simulation and were shocked at how your team managed to stop the attack in 40 minutes. However, for the first 20 minutes, everyone was just looking at the screen, waiting for some alerts to appear. It would be nice to somehow reduce this huge delay, what do you think?" 

Problematic Metric: 

Time to Detect of 20 minutes led to a delayed alert triage. 

Improvement Task: 

Tune the SIEM and the detection rules to run more often, every 5 minutes. There is a problem involving the alert appearing for the L1 analysts. 

Assign Task To: 

Assign the detection rule's schedule review to the dedicated SOC engineers. 

The Third Complaint: 

"Dear SOC manager, on behalf of all L1 analysts, I want to raise an issue that may require your help. On average, during an 8-hour shift, our L1 analysts close 760 alerts, 95% of which is system noise from our IT team or automation scripts. It is impossible to perform a vigilant triage with such a big load, and analysts are starting to get exhausted. Moreover, as the company grows, we receive more and more alerts. Can you help us with it, please?" 

Problematic Metric: 

False Positive Rate is the core of the problem. There is too much noise that the L1's have to sift through to actually find the alerts that actually require attention.

Improvement Task: 

Schedule a call with the team to implement the False Positive remediation process. 

Assign Task To: 

Assign the task to SOC engineers to exclude the system and IT noise from the rules. It significantly reduces FP alerts. 

I was successfully able to choose the correct choices across the three scenarios on my first attempt. 

<b>Task 5: Conclusion</b> 

In this lab I learnt about the core internal metrics, and the key performance metrics that are often featured in Service Level Agreements. Additionally, I briefly explored what it's like to be in the shoes of a SOC manager trying to help their team improve their key performance metrics's by partaking in the interactive practice scenarios. 

## Sources 

TryHackMe, n.d., SOC L1 SOC Metrics and Objectives, TryHackMe website, accessed 23 July 2026, Available: <https://tryhackme.com/room/socmetricsobjectives>



