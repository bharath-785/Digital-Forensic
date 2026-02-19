🔍 Live System Analysis & Malware Investigation:

This project demonstrates a full live incident response workflow performed on a Windows virtual machine after a suspicious executable (LairNetPutty.exe) was discovered on a corporate workstation. The goal of the lab was to determine whether the file posed a threat and to document the investigative process using real forensic tools.

🧭 Project Overview:

An employee downloaded an unknown utility without IT approval. As part of the incident response team, I performed a structured investigation that included:

 1. Static analysis of the executable
 2. Dynamic monitoring of system behavior
 3. Network forensics using NETSTAT and Wireshark
 4. Threat intelligence validation using VirusTotal
 5. Assessment of malicious indicators such as suspicious IP connections and retransmission patterns
    
This lab simulates a real-world scenario where responders must quickly evaluate a potentially malicious file while the system is still running.


🛠️ Tools & Techniques Used:

1. Task Manager — Process monitoring and baseline comparison
2. NETSTAT — Active connection analysis and identification of suspicious remote hosts
3. Wireshark — Packet capture, TCP analysis, retransmission investigation
4. VirusTotal — Multi‑vendor malware detection and threat classification
5. OSINT sources — IP reputation checks and community threat reports

🧪 Key Activities Performed:

1. Observed system processes before and after executing the suspicious file
2. Identified unexpected outbound connections to high‑risk IP addresses
3. Captured and analyzed network packets to detect anomalies
4. Investigated repeated TCP spurious retransmissions
5. Verified malware classification through VirusTotal (60/67 vendors flagged it)
6. Researched community reports linking the file to Trojan‑based behavior

🚨 Findings:

  1. The executable exhibited malicious characteristics consistent with Trojan malware.
  2. Multiple antivirus engines classified the file as Backdoor, Trojan, or File Infector.
  3. The system attempted to communicate with known malicious IP addresses, including those associated with suspicious activity reports.
  4. Wireshark revealed repeated spurious retransmissions, suggesting abnormal or blocked communication attempts.
  5. The behavior aligned with malware attempting to establish remote access or command‑and‑control communication.

📘 What I Learned:

  1. How to perform live forensic analysis without shutting down the system
  2. How to use Wireshark to interpret TCP behavior and retransmission patterns
  3. How to validate suspicious files using VirusTotal and OSINT
  4. How to correlate process activity, network behavior, and threat intelligence
  5. How malware disguises itself as legitimate software to evade detection
