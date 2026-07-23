## SOC Workbooks and Lookups 

<b>Difficulty: Easy</b> 

<b>Date Completed: 23/07/2026</b>  

<b>What did I learn:</b> 

- Familiarity with SOC investigation workbooks
  
- Wwhere to find and how to use asset inventory in SOC
  
- Understood the importance of corporate network diagrams
  
- Practical building a workflow inside THM's interactive interface
- 
<b>Prerequisites</b> 

- SOC L1 Alert Triage & Alert Rerporting Rooms 

<b>Tools</b> 

- THM Workbook Practice Site

- 
## The Process: 

<b>Task 1: Introduction </b> 

I learnt what a SOC workbook is. According to THM, a SOC workbook is "designed to streamline alert triage and explains various lookup methods to quick;y retrieve user and system content". 

<b>Task 2: Assets & Identities </b> 

Learnt what an "Identity Inventory" and "Asset Inventory" is, and their purpose. 

It showed me a scenario about one user logging into a server named "HQ-FINFS-02" late at night, and sharing a financial report to another user. Identity and Asset Inventories are used to determine if a scenario like this is expected or not. 

Identity and Asset inventories are essentially a table of information about users and access. Upon looking at the Identity Inventory, the first user's role was "Chief Financil Officer", and he's located in Europe. The second user is a US Financial Advisor located in Texas. Upon finding out this information, it is expected that the CFO would be sharing documents late in the night as he's in a different time zone. 

The Asset Inventory is a list of all the computing resources within an organisation's IT environment, there I foud out that HQ-FINFS-O2 is located in a UK Data center, and it's purpose is to be a file server for financial records. It would make sense as to why the CFO is using this resource. 

<b>Task 3: Network Diagrams </b> 

A network diagram is anover way to gather vital information. sometimes you may need a network diagram to understand an alert. Especially when working for bigger companies. 

<img width="753" height="591" alt="image" src="https://github.com/user-attachments/assets/063d2c94-1720-429f-a28d-f653a599f6da" />

<sub> This is an example of a network diagram I found featuring various subnets, and their corresponding IP address range. (ResearchGate, n.d.)

<b>Task 4: Workbooks Theory </b> 

To avoid missing vital details and confusing attack evidence, sometimes it may require dozens of essential steps that may be difficult for SOC Analysts to remember. SOC Workbooks are a structured document that shows structured steps on how to investigate and remediate specific cyber threats in an effective and consistent way. They resemble a flow chart. Following these steps in the correct order guarantees high-quality alert triage, and removes problems where an incorrect verdict is made without enough evidence. 

There are typically three stages in a workbook. 

- Enrichment: Using threat intelligence and resources like Identity / Asset Inventory and Diagrams to gather intel.

- Investigation: Making your verdict using the gathered data and SIEM logs.

- Escalation: Escalating the alert to L2 or communicating with the affected users / handlers of the affected asset. 


<b>Task 5: Workbooks Practice </b>  

In the final task, I was provided by THM with practice creating 3 different workbooks by dragging and dropping steps into their correct location on the flowchart. 

Workbook 1 (Email Analysis): 

This workbook takes you through effective email analyise. By first assigning the alert to yourself
, and then gather intel about the email using EML analysers. Then go through attatchement analysis, like using sandboxes and manual code reviews for anything malicious. 

Using the analysis, make a verdict of whether the attatchement turned out to be malicious, or if the email's origin is spoofed / unexpected for the roles of the recipient. Depending on the verdict, choose the next steps. Whether that's closing the alert as a "False Positive" while explaining why the email is safe and expected under the alert comments. Or go through the alert reporting and triaging and reporting process to escalate the situation to L2.


<img width="1107" height="859" alt="image" src="https://github.com/user-attachments/assets/2d3d97a7-e4bd-4906-bd18-c9dd813ce258" />

<sub>Workbook 1 (THM, n.d.)</sub>

Workbook 2 (PowerShell Analysis) : 

This workbook is about an alert regarding a potentially malicious executible. It goes through the steps of assigning the alert yourself. First going through the enrichment stage by gathering intel about the affected machine using asset inventory, and then using threat intelligence to analyse the URL, and perfoming static analysis of the downloaded executable using web-based services like VirusTotal. The next step is to find out the parent process and the account that executed the potentially malicious script by building a process tree.  

Using these resources for your investigation, make a verdict of whether the file is or isn't malicious, and follow the required steps based on that verdict. 


<img width="768" height="610" alt="image" src="https://github.com/user-attachments/assets/dbfbeab7-5eec-44a6-9ecc-1091f7af1656" />


<sub>Workbook 2 (THM, n.d.)</sub> 

Workbook 3 (Network Analysis): 

Assign the alert to yourself, gather the relevent information using network diagrams and asset inventory. In this scenario it's listing the ports that was scanned by a potentially malicious IP, and finding the services that correlate to those ports. If the service is a vulnerability scanner, confirm if the types of scanning it does is expected.  IF the verdict is FP, contact the SOC engineers to tune the rules so that it mitigates the alert from happening again. Or if it's True Positive, then report, and escalate to L2. 

<img width="768" height="629" alt="image" src="https://github.com/user-attachments/assets/160e42bc-2352-4c8b-a86b-4a96eccc7987" />


<sub>Workbook 3 (THM, n.d.)</sub>

## Sources 

ResearchGate, n.d., Metwprl diagram of the enterprise network used in the experiment, ResearchGate website, accessed 23 July 2026, Avaialable: <https://www.researchgate.net/figure/Network-diagram-of-the-enterprise-network-used-in-the-experiment_fig3_288208464>

TryHackMe, n.d., SOC L1 SOC Workbooks and Lookups, TryHackMe website, accessed 23 July 2026, Available: <https://tryhackme.com/room/socl1alertreporting>

