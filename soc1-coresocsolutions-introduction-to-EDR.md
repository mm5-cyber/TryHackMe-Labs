## Introduction to EDR 


<b>Difficulty: Easy</b> 

<b>Date Completed: 24/07/2026</b>  

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

- Anomaly Detection

- IOC matching

- MITRE ATT&CK Mapping

- Machine Learning Algorithms


<b>Response</b> 

After detection, comes response. EDR's offer both automated and manual responses. You can configure your own policies to block malicious behaviours automatically. With manual response, you are given a wide range of capabilties to make use of. These of which are: 

- Isolate Host

- Terminate Process

- Quarantine

- Remote Access

- Artefacts Collection

<b>Task 7: Investigate an alert on EDR (Practical</b> 

This task took me through the role of a SOC Analyst at a company called TECH THM. I'm given access to an EDR console that is currently showing multiple medium and high-severity detections. What I'mt asked to do is to perform triage on each detection using the information provided in the EDR. 



## Sources 

Palo Alto Networks, n.d., What is EDR vs Antivirus, Palo Alto Networks websites, viewed 24th July 2026, Accessed:  <https://www.paloaltonetworks.com/cyberpedia/what-is-edr-vs-antivirus>

