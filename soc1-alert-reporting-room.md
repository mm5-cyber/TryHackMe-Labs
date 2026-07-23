
## Room Name: SOC L1 Alert Reporting 

<b>Difficulty: Easy</b> 

<b>Date Completed: 22/07/2026</b>  

<b>What did I learn:</b> 

- The proper format for for SOC alert reporting and escalation  

- Confidence in using a SOC Simulator Dashboard
 
- How to apply the knowledge to triage alerts in a simulated environment

<b>Prerequisites</b> 

- SOC L1 Alert Triage Room 

<b>Tools</b> 
- THM SOC Dashboard

## The Process: 

<b>Task 2: Alert Funneling </b> 

The lab tought me about the Alert Funnel, which is a SOC filtering process where massive amounts of raw telemetry and security events are funneled down into a highly manageable number of actual security incidents. Below is an image of what the alert funnel looks like: 

<img width="780" height="366" alt="image" src="https://github.com/user-attachments/assets/13b342a6-8db0-4d12-b228-c0eb7f1c27d6" /> 
<sub>Alert Funnel (THM) </sub>  


As a SOC L1 Analust, you need to be able to send alerts for complex security incidents further down the funnel to the L2 Analyst using three methods. 

- Alert Reporting:
  
Documentining your investigation in detail, and including relevent evidence. This is especially important if the investigation is about a "True Positive" alert, which may require escalation to a L2 analyst. 

- Alert Escalation
  
Transfer the alert to a L2 analyst along with the relevent documentation about it that you createed during the alert reporting process. This improves efficiency, so that the L2 Analyst doesn't have to spend too much time analysing the alert from scratch. Essentially, it gives them an idea on what the alert is about.  

- Communication

During or after the analysis, it is important to communicate with the other departments. Like the HR Department for info about users, or the IT department for confirmation if they have granted privileges to certain users or groups. 


<b>Task 3: Reproting Guide </b>

Reporting is especially important as it provides context for escalation, save findings for records, and improves the investigation skills of L1 Analysts. 

For the format of the report, TryHackMe reccomends to include the five W's whenever possible. These of which are "Who, What, When, Where, and Why". I also followed the Alert Report Checklist to make sure that my report provides as much information as possible to the L2 Analyst. 

<img width="408" height="599" alt="image" src="https://github.com/user-attachments/assets/e800b5be-1a00-46b9-a432-698ea115d1d5" />

<sub>Alert Report Checklist (THM)</sub> 

Using this info, I was prompted to open the THM SOC Dashboard and write a report for an email marked as "phishing", after it had already been sent to the recipient. 

Here is the SIEM findings:

<img width="1619" height="361" alt="image" src="https://github.com/user-attachments/assets/daf8620d-40aa-4ad0-bbe3-de9f8a906518" />

While analysing the findings, I set myself as the assignee, and changed the status from "awaiting action" to in-progress. As seen below: 

<img width="660" height="474" alt="image" src="https://github.com/user-attachments/assets/59de8126-f3c0-408d-b77b-05b8338c25af" /> 
<sub> Assigning myself to the alert, and changing the status to "in-progress"</sub>

here is what I wrote in my alert report, I ensured that I followed the Alert Report Checklist: 

<img width="691" height="375" alt="image" src="https://github.com/user-attachments/assets/7d53bb50-0fcb-42a0-8bfe-ad9367ffed66" />

I then escalated the alert. I set the assignee to a L2 Analyst, kept the status set to "In Progress", as it's still ongoing. I then set the verdict to "True Positive", as the activity is deemed as malicious, and requires L2 expertise. 

<img width="653" height="468" alt="image" src="https://github.com/user-attachments/assets/d03041c8-956a-45d0-86d1-e21bc077aef6" />

<sub>My alert report and escalation submission</sub> 
 

<b>Task 4: Escalation Steps </b> 

This part of the room taught me about whether or not I should escelate the alert. I learnt that you should escalate the alerts if: 

1. The alert is an indicator of a major cyberattack requiring deeper investigation or DFIR
2. Remediation actions like malware removal, host isolation, or password reset are required
3. Communication with customers, partners, management, or law enforcement agencies is required
4. You just do not fully understand the alert and need some help from more senior analysts

In most cases, escalating a report requires you to reassign the alert to a L2 analyst, and ping them in a corporate chat or notify them in person. Though escalation methods differ depending on the workplace. 

<b> Alert Report 2: Spike of Domain Discovery Commands </b> 

This is the alert that I was tasked with managing: 

<img width="1253" height="468" alt="image" src="https://github.com/user-attachments/assets/eb10d178-d87e-43d8-9983-60632857d524" />

Here is what I wrote for the report: 

<img width="681" height="303" alt="image" src="https://github.com/user-attachments/assets/506fd616-2b80-4f8d-bb6f-e6a10ccddfa3" />

I assigned the alert to L2, changed the verdict to "True Positive". Additionally, I changed the Severity from "Medium" to "Critical" as a compromised user with authority on an a Windows Server is an emergency-level response. 

<img width="664" height="467" alt="image" src="https://github.com/user-attachments/assets/9938c0d4-279c-41a0-a709-417c30c2fd7e" /> 

<sub>My alert report and escalation submission</sub> 

<b>Task 5: SOC Communication</b> 

This last section of the room is about preparing for unexpected scenarios amd knowing what to do in the event of a critical event. In most workplaces, the SOC team has its own "Crisis Communication" Procedures. However, it is still important to review communication cases to be prepared to handle these scenarios effectively. These are examples provided by THM. 

Here are some "Communication Cases" examples: 

<img width="820" height="376" alt="image" src="https://github.com/user-attachments/assets/0cea4720-c58c-49d3-a5f9-9c216e85c37c" />
<sub>Communication Cases (THM) </sub> 

## Sources 

TryHackMe, n.d., SOC L1 Alert Reporting, TryHackMe website, accessed 22 July 2026, Available: <https://tryhackme.com/room/socl1alertreporting>





