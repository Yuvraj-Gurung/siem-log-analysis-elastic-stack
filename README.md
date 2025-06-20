# **SIEM Log Analysis Documentation**

## **1. Project Overview**  
### **Project Name:** SIEM Log Analysis  
### **Objective:**  
The goal of this project is to analyze security logs using a Security Information and Event Management (SIEM) system, detect suspicious activities, and enhance threat intelligence. This includes collecting logs from various sources, correlating events, and responding to potential security incidents.

## **2. Tools & Technologies Used**  
- **Ubuntu:** Used as a SIEM server running Elastic Stack.  
- **Windows Server 2022:** Generates logs for security events, authentication attempts, and system behavior.  
- **Elastic Stack (ELK):** Logs collection, parsing, visualization, and correlation.  
- **Mythic C2 Server:** Simulates attacker operations and persistence mechanisms for adversarial emulation.  
- **Metasploit Framework:** Used to generate attacks and assess system vulnerabilities.  
- **Sysmon:** Provides detailed system monitoring to capture process creations, network connections, and registry changes.  

## **3. System Setup & Configuration**  
### **3.1 ELK Stack Configuration**  
1. Install **Elasticsearch**, **Logstash**, and **Kibana** on Ubuntu.  
2. Configure Logstash to ingest logs from Windows Server.  
3. Deploy **Winlogbeat** on Windows Server to ship event logs.  
4. Create SIEM dashboards in Kibana for log visualization.  

### **3.2 Windows Server 2022 Logging**  
1. Install **Sysmon** to enhance log visibility.  
2. Enable **audit policies** for login attempts, privilege escalations, and system modifications.  
3. Set up **Event Forwarding** to send logs to ELK Stack.  

### **3.3 Threat Simulation with Metasploit & Mythic C2**  
1. Set up Mythic C2 for Red Team simulations.  
2. Launch Metasploit attacks (e.g., privilege escalation, remote execution).  
3. Capture logs generated from exploits and correlate findings in SIEM.  

## **4. Log Analysis & Findings**  
### **4.1 Detecting Suspicious Events**  
- Identified **failed login attempts** and potential brute-force attacks.  
- Observed **process injections** and unexpected PowerShell executions.  
- Monitored **unusual outbound connections** originating from the compromised system.  

### **4.2 Correlation of Events**  
- Mapped attack patterns using **Kibana dashboards**.  
- Used **Logstash filters** to extract Indicators of Compromise (IoCs).  
- Analyzed timestamps to track attacker movements.  

## **5. Conclusion & Future Improvements**  
- The project demonstrated how SIEM can detect cybersecurity threats in real-time.   
- Expanding log sources to include **firewall logs and threat intelligence feeds**.



## *Walkthrough | Screenshots*

**Elastic (ELK) Stack Installation**

<img src="project/image1.png"> <img src="project/image2.png"> <img src="project/image3.png"> <img src="project/image4.png"> <img src="project/image5.png"> <img src="project/image6.png"> <img src="project/image7.png"> <img src="project/image8.png"> <img src="project/image9.png"> <img src="project/image10.png"> <img src="project/image11.png"> <img src="project/image12.png"> <img src="project/image13.png"> <img src="project/image14.png"> <img src="project/image15.png">

**Mythic C2 Server Installation**

<img src="project/image16.png"> <img src="project/image17.png"> <img src="project/image18.png"> <img src="project/image19.png"> <img src="project/image20.png"> <img src="project/image21.png"> <img src="project/image22.png"> <img src="project/image23.png"> <img src="project/image24.png"> <img src="project/image25.png">

**Sysmon Installation**

<img src="project/image26.png"> <img src="project/image27.png"> <img src="project/image28.png"> <img src="project/image29.png"> <img src="project/image30.png"> <img src="project/image31.png"> <img src="project/image32.png"> <img src="project/image33.png"> <img src="project/image34.png">

**Elastic Fleet and Agent Installation**

<img src="project/image35.png"> <img src="project/image36.png"> <img src="project/image37.png"> <img src="project/image38.png"> <img src="project/image39.png"> <img src="project/image40.png"> <img src="project/image41.png"> <img src="project/image42.png"> <img src="project/image43.png"> <img src="project/image44.png">

**Ingesting Windows Defender and Sysmon Logs to Elasticsearch**

<img src="project/image45.png"> <img src="project/image46.png"> <img src="project/image47.png"> <img src="project/image48.png"> <img src="project/image49.png"> <img src="project/image50.png"> <img src="project/image51.png"> <img src="project/image52.png"> <img src="project/image53.png"> <img src="project/image54.png">

**Mythic C2 Agents/C2 Profiles Installation**

<img src="project/image55.png"> <img src="project/image56.png"> <img src="project/image57.png"> <img src="project/image58.png"> <img src="project/image59.png"> <img src="project/image60.png"> <img src="project/image61.png"> <img src="project/image62.png"> <img src="project/image63.png"> <img src="project/image64.png"> <img src="project/image65.png">

**Bruteforcing RDP | Disabling Windows Security**

<img src="project/image66.png"> <img src="project/image67.png"> <img src="project/image68.png"> <img src="project/image69.png"> <img src="project/image70.png"> <img src="project/image71.png"> <img src="project/image72.png"> <img src="project/image73.png"> <img src="project/image74.png"> <img src="project/image75.png"> <img src="project/image76.png"> <img src="project/image77.png">

**Mythic C2 Exploitation/Command and Control**

<img src="project/image78.png"> <img src="project/image79.png"> <img src="project/image80.png"> <img src="project/image81.png"> <img src="project/image82.png"> <img src="project/image83.png"> <img src="project/image84.png"> <img src="project/image85.png"> <img src="project/image86.png"> <img src="project/image87.png"> <img src="project/image88.png"> <img src="project/image89.png"> <img src="project/image90.png"> <img src="project/image91.png"> <img src="project/image92.png"> <img src="project/image93.png"> <img src="project/image94.png"> <img src="project/image95.png">

**Investigating Mythic C2 Payload**

<img src="project/image96.png"> <img src="project/image97.png"> <img src="project/image98.png"> <img src="project/image99.png"> <img src="project/image100.png"> <img src="project/image101.png"> <img src="project/image102.png">

**Generating Metasploit Payload**

<img src="project/image103.png"> <img src="project/image104.png"> <img src="project/image105.png"> <img src="project/image106.png">

**Elastic Defend Integration**

<img src="project/image107.png"> <img src="project/image108.png"> <img src="project/image109.png"> <img src="project/image110.png"> <img src="project/image111.png"> <img src="project/image112.png"> <img src="project/image113.png"> <img src="project/image114.png"> <img src="project/image115.png"> <img src="project/image116.png"> <img src="project/image117.png"> <img src="project/image118.png"> <img src="project/image119.png">

**Investigating Metasploit Payload**

<img src="project/image120.png"> <img src="project/image121.png"> <img src="project/image122.png"> <img src="project/image123.png"> <img src="project/image124.png">








