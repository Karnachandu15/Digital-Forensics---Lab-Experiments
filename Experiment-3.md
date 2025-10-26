# Experiment - 3 
# Capture and Analyze Network Traffic using Wireshark  

## Aim  
To capture live network traffic and analyze the captured packets using **Wireshark**, a widely used network protocol analyzer.  

---

## Description  
In digital forensics and cybersecurity, analyzing network traffic is a crucial step to detect suspicious activities, investigate security incidents, and understand communication patterns. Wireshark is an open-source packet analyzer that allows investigators to capture live network packets and analyze them in detail.  

This experiment demonstrates how to use Wireshark to capture network traffic, filter relevant protocols, and interpret packet details for forensic analysis.  

---

## Tools & Equipment Used
 - Wireshark(software)


## Link to download Wireshark
[Click to download](https://2.na.dl.wireshark.org/win64/Wireshark-4.4.9-x64.exe)

## Procedure  

**Launch Wireshark**  
   - Open Wireshark with administrative privileges.
 ![alt text](<Output Screenshot/Exp3/Screenshot (73).png>) 

   - The home screen displays all available network interfaces. 

     

**Select a Network Interface**  
   - Choose the appropriate interface (e.g., Wi-Fi, Ethernet).

   - Double-click the interface to start capturing packets.  

 

**Start Packet Capture**  
   - Wireshark begins displaying live packet data in real time. 
![alt text](<Output Screenshot/Exp3/Screenshot (74).png>)

   - Each packet shows **Time, Source, Destination, Protocol, and Info**.  
![alt text](<Output Screenshot/Exp3/Screenshot (79).png>)

**Apply Capture/Display Filters**
   - Use filters to focus on specific traffic. Examples:
     - `http` → only HTTP traffic
    ![alt text](<Output Screenshot/Exp3/Screenshot (76).png>)

     - `tcp.port == 80` → traffic on TCP port 80
    ![alt text](<Output Screenshot/Exp3/Screenshot (77).png>)

     - `ip.addr == 10.2.24.13` → traffic to/from a specific IP 
  

**Inspect Individual Packets**  
   - Select a packet to view its details.    

   - The breakdown shows Ethernet, IP, TCP/UDP, and application layer data.

   - Raw packet data is displayed in hexadecimal/ASCII format.
![alt text](<Output Screenshot/Exp3/Screenshot 2025-08-31 223412.png>) 
     

**Save the Capture File**  
   - Save in `.pcapng` format for later analysis.

   - Go to **File → Save As** and give a suitable name.  
![alt text](<Output Screenshot/Exp3/Screenshot (80).png>)
  

**Analyze Captured Traffic**  
   - Study protocols, packet sizes, and flows.

   - Look for anomalies like failed connections, unusual IPs, or suspicious activity.  

---

## Result  
Network traffic was successfully captured and analyzed using Wireshark. The experiment demonstrated how to filter packets, inspect protocol details, and save capture logs for forensic investigation.  

---
