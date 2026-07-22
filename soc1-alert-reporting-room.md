
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
  
