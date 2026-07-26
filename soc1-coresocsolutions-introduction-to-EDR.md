## Introduction to EDR 


<b>Difficulty: Easy</b> 

<b>Date Completed: 26/07/2026</b>  

<b>What did I learn:</b> 

- The basics of EDR and how it works
  
- How EDR is different from traditional Antivirus solutions
  
- The Architecture of an EDR solution through examination
  
- Analysing the types of telemetry that EDR collects from endpoints
  
- Understood the detection and response capabilities of an EDR

- Investigated a realistic alert in an EDR.
- 
<b>Prerequisites</b> 

- Basic knowledge of different endpoints (Windows, Linux Mac), as well as the common attacks associated with them.

- Basic awareness of the role of a SOC team


## The Process 

<b>Task 1: Introduction</b> 

In the introduction, I learnt the definition of Endpoint Detection and Response (EDR). According to THM, it is a "security solution designd to monitor, detect, and respond to advanced threats at the endpoint level." It is a widely adopted solution within organisation's that are used to protect endpoint devices. 

<b>Task 2: What is an EDR?</b> 

Along with the increase in use of digital devices being used as core functions within many businesses. Cyber threats, are also increasing every day. Business implement security measures to protect their assets on a network level. However, with the rise of remote work, many devices that are outside that perimeter of protection are exposed to cyber attacks. 

EDR is a solution that is implemented to ensure that the devices that are outside of the network, are safe. EDR is a security solution that is built to offer deep-level protection specifically for end devices. Threats will be constantly monitored and detected regardless of where the device may be located. 

There are many different EDR solutions that are available in the market. The features that they provide may differ, but their underlyying architecture is usually very similar. Some of these solutions are as follows: 

- CrowdStrike Falcon

- SentinelOne ActiveEDR

- Microsoft Defender for Endpoint

- OpenEDR

- Symantec EDR.


There are three main features present wihtin an EDR. They are also known as the three pillars of an EDR Solution. These of which are Visibility, Detection, and Response. I will explain each of these in detail below:  

<b>Visibility</b>

An EDR provides a very impressive level of visibility for an end deice. It collects detailed data from the endpoints, such as process modifications, registry modifications, file and folder modifications, the user actions, and more. It is all presented in a structured format so that the analyst can easily understand what is going on. Context is provided for any detection within an EDR. 

An example of visibility is the process tree. The EDR creates a graphical representation of a process tree. This features nodes which represents a certain process. To show the relationship between the nodes, they are connected by lines. In addition, each node has a "+" icon that allows you to delve into that node and see what exactly is happening. For example, you can see the network connnections, registry changes, file changes, etc. 

<img width="1911" height="597" alt="image" src="https://github.com/user-attachments/assets/17ed0c6c-0e6b-44a4-97cc-1765dc3a1fc6" />

<sub>A graphical representation of a process tree within an EDR solution (THM, n.d.)</sub>

This is just one of the visibility features within an EDR, there are many more.  

<b>Detection</b>

the detection capabilities of an EDR include both signature-based detections and behaviour-based detections. They are two two core methods used in cybersecurity to spot and stop threats. 

Signature-based detections compares data like files, codes, or network traffic against a giant list of known threat signatures. If anything matches, then it is flagged. 

Behaviour-based detection monitors how a program, user, or device usually acts. If anything happens out of the blue then it is flagged. 

the screenshot below provided by THM shows a dashboard, this is very similar to a SIEM dashboard which I have become familiar with. It features fields like the severity of an alert, when it was detected, what processes on the host the alert is tied to, what the tactic via technique it is, along with command line info. 

<img width="1917" height="738" alt="image" src="https://github.com/user-attachments/assets/4c26fad2-6ac6-4eec-b2be-9314d95bbbe1" />

<sub>EDR Dashboard (THM, n.d.)</sub>

<b>Response</b>

Response is the last pillar of the EDR Solution. It is a feature that allows hte analysts to actually respond and remediate the detected threats. Actions can be taken for any endpoint device that is situated within a central EDR console. You can choose to do things like isolate an endpoint, terminate a process, or quarantine files. Additionally, you can remotely connect to the device, abd do things there from within the EDR console. 

This screenshot providede by THM shows an example of connecting to an end device from within the EDR console and executing an action like running scripts. 

<img width="1919" height="862" alt="image" src="https://github.com/user-attachments/assets/5c8dd30e-39f3-4ae9-9af6-2a4931fd59d2" />

<sub>As shown in CrowdStrike Falcon, you can connect to a device remotely and execute actions from the EDR console (THM, n.d.)-</sub>

It is important to remember that an EDR is a host-only security solution. Therefore it doesn't detect any network level threats. 

<b>Task 3: Beyond the Antivirus</b>

I then learnt about how an EDR is different from a typical antivirus. Before this lab I thought they were pretty similar. They both share in common the same motive of protecting the endpoint on which they are installed on. 

Traditional antivirus's follow basic detection rules to block and remove known malware. However EDR's constantly monitoring, they are like a surveillance system that looks out for unusual activity and reports them (Palo Alto Networks, 2026). 

<b>Task 4: How an EDR works?</b>

In this task, these questions were answered: 

- How does an EDR manage to provide this much visibility of the endpoints?

- How can it detect advanced threats?

- How can a few clicks eradicate the threat from an endpoint?

<b> EDR Agents </b>
EDR uses EDR agents that are deployed inside the endpoints. They are essentially sensors. They sit at the endpoint and monitor all activities, collecting information in detail and then sending them to the EDR console in real time. Additionally, these agents perform basic tasks like signature, and behaviour-based detections, whic are then sent to the EDR console, triggering alerts. 

<b> EDR Console </b> 

All the detailed data collected by the EDR agents are sent and anlysed through complex logic and machine learning algorithms within the centralised EDR Console. There, threat intelligence information is matched with the collected data to detect any threats. Thus, sending an alert. Essentially, the EDR Console is the brain. 

Below is an EDR Console Dashboard, it puts all the incoming data together. It provides charts and tables of information, showing the current status of detections within all the endpoints. 

<img width="2530" height="1204" alt="image" src="https://github.com/user-attachments/assets/a41938a9-3ea0-4f4d-b44c-cddda1b8ef06" />

<sub> EDR Console Dashboard (THM, n.d.) </sub> 

<b> What happens after detection</b>

Based on the data provided by the EDR Console, it is up to the SOC analyst's to use their expertise to form a verdict of whether an alert is a false positive or true positive. In the event of a true positive, analysts can initiate remediation within the EDR console. 

<b> EDR with Other Tools </b> 

EDR tools can work alongside other security solutions to form a larger security ecosystem. For example, in a network there are firewalls, DLPs, Email Security Gateways, IAMs. These along with the EDR's are integrated into a SIEM solution. Which is what the analysts will be using for their investigations. 

<b>Task 5: EDR Telemetry</b> 

In this task, I learnt what exactly is telemetry, and how they are collected. 

<b> What is Telemetry? </b> 

It is essentially the data that is collected by the EDR agents, and sent to the EDR console. According to THM, telemetry is "the black box of an endpoint with everything necessary for detection and investigation" (THM, n.d.). 

<b> Collected Telemetry </b> 


When it comes to being able to differentiate regular and malicious activity, better judgements can be made when more data is collected. 

EDR collects 'detailed' telemetry from the endpoints. Some of the telemtry that it collects are: 

- Process Exeecutions and Terminations
  
   EDR monitors all of the running and idle processes within an End device. These help identify things like any processes that were initiated through a suspicious process, questionable child-parent process relationships, malware payloads etc. 

- Network Connections
Endpoint network connections are monitored to identify things like connections to a Command & Control server, detect unusual port usage, signs of data exfiltration, or lateral movement within the network. 

- Command Line Activity

Identifies signs of malicious command execution, and obfuscated powershell script executions by capturing all the commands executed on the endpoint. 

- Files and Folders Modifications

These should be monitored as threat actos make changes to files and folders to do things like execute ransomware, malicious file dropping, and data staging. Data staging is when threat actors bundle stolen files into a temporary folder before exfiltrating it. 

- Registry Modifications

The registry acts as a central database for configuration settings, system behavior, and startup applications within a Windows endpoint. That is why malware frequently targets the registry to modify these settings and behaviours for the benefit of the malicious user. 


The activities created through advanced threats may seem harmless. But when observed through detailed telemetry, that is when the bigger picture can be found, and verdicts can be made. 

<b>Task 6: Detection and Response Capabilities</b>

This task highlights advanced detection techniques and the response mechanisms of an EDR.

Some advanced detection techniques are: 

- Behavioral Detection

Observes the complete behaviour of a file. EDR catches malicious behaviours from malware that were designed to look like clean and legitimate processes.

An example is winword.exe spawning powershell.exe. It's flagged because it is an unusual parent-child relationship. 

- Anomaly Detection

Overtime, the EDR will start understanding the behaviours of an endpoint. Any activities that deviate from the regular behaviour will be flagged.  

- IOC matching
The EDR will flag anything that matches indicators published on threat intelligence feeds.

- MITRE ATT&CK Mapping
A flagged EDR will include a "MITRE Tactic and Technique" section that provides info on what and how something is being attacked.

- Machine Learning Algorithms
Modern EDR's contain machine learning models that are trained on a large dataset regarding the normal and malicious behaviours. It's used to detect complex attack patterns.

Complex attacks like fileless attakcs and multi-staged intrusions are detected through this feature. 
<b>Response</b> 

After detection, comes response. EDR's offer both automated and manual responses. You can configure your own policies to block malicious behaviours automatically. With manual response, you are given a wide range of capabilties to make use of. These of which are: 

- Isolate Host

- Terminate Process

- Quarantinining Malicious Files

- Remote Access
For deeper visibility or to execute custom actions) 

- Artefacts Collection
Extracting data from the endpoints for detailed forensic investigation or reporting. Artefacts that are most commonly extracted are Memory Dumps, Event Logs, Specific Folder Contents, and Registry Hives.

<b>Task 7: Investigate an alert on EDR (Practical</b> 

This task took me through the role of a SOC Analyst at a company called TECH THM. I'm given access to an EDR console that is currently showing multiple medium and high-severity detections. What I'mt asked to do is to perform triage on each detection using the information provided in the EDR.  

<img width="715" height="1209" alt="image" src="https://github.com/user-attachments/assets/fd3e8506-afcf-49a8-8f40-72edc1ddef9b" /> 

<sub>This is what the simulated EDR Dashboard looks like (THM, n.d.) </sub>


Question1 : Which tool was launched by CMD.exe to download the payload on DESKTOP-HR01? 

As seen on the dashboard image, I navigated to the most recent detection, with the targetted host being DESKTOP-HR01. 

Below you can see the whole process chain of the attack. After opening a macro-enabled document, Winword.exe spawned a command terminal, which then downloaded a malicious file through curl, which provided access to the machine for the threat actor. 

<img width="713" height="930" alt="image" src="https://github.com/user-attachments/assets/ebff45b9-04d1-4334-b36e-e3285a356ebf"/> 

<sub>Process Info tab of the "Initial Access via Malicious Office Document"</sub> 

The answer is: cURL.exe. The child process of cmd.exe in this scenario. 

Question 2: What is the absolute path to the downloaded malware on the DESKTOP-HR01 machine?

<img width="711" height="638" alt="image" src="https://github.com/user-attachments/assets/c614576a-a245-4385-9685-8b8210f656dd" /> 

<sub>IOC/Indicators tab of the alert (THM, n.d.)</sub>

Q2 AnswerL I navigated to the IOC/Indicators tab on that same alert and found the file path of the downloaded malware, which is C:\Users\Public\install.exe. The name of the malicious file is simply "install.exe".

Question 3: What is the absolute path to the suspicious syncsvc.exe on the WIN-ENG-LAPTOP03 machine? 

I navigated to the second alert within the EDR Dashboard. This alert is titled "Credential Dumping via LSASS Memory Access". The summary indicates that the alert is a suspicious behavuour found in memory dumps. An Unsigned binary (syncsvc.exe) launched from a temp directory and accessed the core process lsass.exe". Then the device made an attempt to access an outbound network, which was blocked. Most likely to send whatever it tried to steal.  


I did some clarifing google searches, I learnt that an unsigned binary is a software without a cryptographic digital signaturem abd a temporary directory is a dedicated folder on an OS that is regularly used by applications to store short-lived data created during a process, and delted after it's finished. 

The target of the unauthorised memory access "lsass.exe" stands for Local Security Authority Subsystem Service. According to JumpCloud, it is a core windows process for "authentication, authorisation, and credential management. It handles local security policies, user authentication, and stores credentials in memory (JumpCloud, 2026). 

Upon further look at the process chain of this alert, the legitimate explorer.exe process launched the suspicious executible which targetted lsass.exe, and made an attempt to exfiltrate the data to an outbound network. 

<img width="154" height="431" alt="image" src="https://github.com/user-attachments/assets/acc5cfcd-03d8-48e2-a039-7f2c881fcf54" /> 

<sub> Process Chain of "Credential Dumping via LSASS Memory Access </sub>


Within the IOC/Indicators tab, I found where the absolute path of the suspicious syncsvc.exe was on the WIN-ENG-LAPTOP03 machine. 


<img width="726" height="711" alt="image" src="https://github.com/user-attachments/assets/9894d089-51d3-4d70-be70-95a201b6be11" /> 
<sub>IOC/Indicators tab of "Credential Dumping via LSASS Memory Access" Alert.</sub>

Q3 Answer: C:\Users\haris.khan\AppData\Local\Temp\syncsvc.exe

Question 4: On which URL was the exfiltration attempt being made on WIN-ENG-LAPTOP03?

Within the process info, I clicked on the "syncsvc.exe" node on the process chain and I was able to find the exact URL that the data was trying to exfiltrated to. 

<img width="708" height="1099" alt="image" src="https://github.com/user-attachments/assets/5252b9aa-02ee-43d3-93fc-fc8d05c19499" />
<sub>process info of the "syncsvc.exe" node. </sub>

Q4 Answer: https://files-wetransfer.com/upload/session/ab12cd34ef56/dump_2025.dmp 

I then navigated to the alert that targetted the host "DESKTOP-DEV01" for the final question. But first, I wanted to see what the alert is about. 

It was titled "Execution from AppData Discovery". with the summary "An unsigned binary located in the user's AppData folder initiated an outbound HTTP connection. The behavior aligns with patterns often observed in dropper or staging malware."

Dropper and malware staging is a technique used by attackers to deliver and install malicious malware sneakily., hiding it from security tools.  

Under the Process Info, explorer.exe launched user-space binary. This can indicate some legitimate processes, or potential malware persistence abuse, which is the case. 


The threat actors tried to run a fake update agent and make a connection to a certain IP. 

<img width="670" height="664" alt="image" src="https://github.com/user-attachments/assets/d8e9b715-c01b-4eec-b869-a329cc1999f8" />\

<sub>"UpdateAgent.exe" node information (THM, n.d.)</sub>

Question 5: What was UpdateAgent.exe labelled by Threat Intel on DESKTOP-DEV01? 

Question 5 Answer: The image above, revealed the threat intel, which is  "Known internal IT utility tool". This means that the attackers are abusing the name of a legitimate file name for nefarious actions, such as connecting to that external IP. 

## Bonus 

Outside of the questions that I had to answer to complete the THM room, there was another alert that wasn't explored, and I wanted to figure out what happened in the alert. 

The alert was titled "Suspicious Persistence via Scheduled Task". Persistence is essentially what hackers do to stay accessed to a system or network for a long time. 

The targetted Host is "DESKTOP-UATSERVER", and the summary of the alert is "A suspicious executable (svcupdate.exe) was observed creating a scheduled task named “WinUpdateService” for persistence. The binary was unsigned and launched from an unusual path (C:\Users\john\AppData\Local\Temp). Scheduled tasks are a common persistence mechanism leveraged by attackers."

<img width="716" height="977" alt="image" src="https://github.com/user-attachments/assets/e5942040-06ec-4a6e-9ccd-05a4780b8f5b" /> 

<sub>Summary page of the "Suspicious Persistence via Scheduled task aler"</sub>

According to Centri, I learnt that a scheduled task is a built in-operating system feature that automatically runs scripts during certain times (Centri, n.d.).

In this scenario, a malicious executible created a task for the attacker to have future access to the sytem. 






## Conclusion  

This project gave me a clear understanding of how modern EDR solutions work and why they differ from traditional antivirus tools. I explored EDR architecture, the telemetry it collects, and how those data points support detection and response. Investigating a realistic alert helped connect the theory to practical use. Overall, I gained a solid foundation in endpoint security and the role EDR plays in identifying and handling threats.




## Sources 

Centri, n.d., Knock, Knock! Who’s Persisting? Sneaky Secrets in Windows Scheduled Tasks, Centri website, viewed 26th July 2026, Accessed: <https://www.centri.org/blog/posts/persistence-mechanisms-windows-scheduled-tasks>

Jumpcloud, 2026, What Is the Local Security Authority Subsystem Service (LSASS.exe)?, jump cloud website, viewed 26th July 2026, Accessed: <https://jumpcloud.com/it-index/what-is-the-local-security-authority-subsystem-service-lsass-exe>

Palo Alto Networks, n.d., What is EDR vs Antivirus, Palo Alto Networks websites, viewed 24th July 2026, Accessed:  <https://www.paloaltonetworks.com/cyberpedia/what-is-edr-vs-antivirus>

Try Hack Me, n.d., Introduction to EDR, Try Hack Me website, viewed 24th July 2026, Accessed: <https://tryhackme.com/room/introductiontoedrs?vccr=1>

