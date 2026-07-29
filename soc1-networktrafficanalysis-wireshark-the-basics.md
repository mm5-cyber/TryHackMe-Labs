
# Wireshark: The Basics

<b>Difficulty: Easy</b> 

<b>Date Completed: 29/07/2026</b>  

<b>What did I learn:</b> 

- How to navigate and configure Wireshark
- 
- How to Inspect Packets and discover information from the different layers of TCP/IP
- 
- How to apply display filters
 

<b>Prerequisites</b> 

- Networking Module

<b>Tools</b> 

- Wireshark

- THM Lab machine (virtual environment)

  ## Process

  <b>Tool Overview</b>

In this section of THM room, I learnt what exactly Wireshark is. It is one of the most potent traffic analyser tools available. The tool has multiple uses such as:

  - It can be used to detect and troubleshoot various network problems, such as network load failure points and congestion.
  - 
  - Security anomalies, such as rogue hosts, abnormal port usage, and suspicious traffic can be detected.
  - 
  - It can be used to investigate and learn protocol details such as response codes and payload data.


The GUI features a: 

- Toolbar

- Display Filter bAR

- A recent files section

- An interface that captures filters and available sniffing points (network interfaces). To note, a network interface is the actual connection that is between an endpoint device and a network. The software connections like lo, eth0, and ens33 enables networking hardware.

Below is a picture provided by THM, which shows all the main sections within Wireshark's GUI: 

<img width="1558" height="735" alt="image" src="https://github.com/user-attachments/assets/725de9ca-912f-4477-8808-11846131e9b9" />

<sub>Wireshark's GUI and highlighted sections, image provided by THM (THM, n.d.)</sub> 

You can load a packet capture file by using the file menu, dragging and dropping the file into the application, or double-clicking on the file itself to load it into Wireshark to view it's contents (the packets that have been captured). 

Below is the packet capture file "http1.pcapng" loaded into Wireshark, as well as a visual representation of the three different panes: 

<img width="1200" height="460" alt="image" src="https://github.com/user-attachments/assets/0f90be99-6444-4e97-99ad-2e82030690a0" /> 

<sub>A packet capture file opened in Wireshark, and the three different panes (THM, n.d.)</sub>

The three different panes are as followed: 

- Packet List Pane

- Packet Details Pane

- Packet Bytes Pane

