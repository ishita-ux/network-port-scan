# network-port-scan
cyber internship task -network port scanning using nmap
# Task 1 - Local Network Port Scanning

## Objective
To perform network reconnaissance and identify open ports on devices within the local network using Nmap.

---

## Tools Used
- Kali Linux
- Nmap
- Wireshark (Optional)

---

## Network Information
Local IP Range Identified: 192.168.74.0/24  
Environment: VMware NAT Network

---

##  Scan Command Used

TCP SYN Scan:
sudo nmap -sS 192.168.74.0/24

Advanced Scan (Service & OS Detection):
sudo nmap -sS -sV -O 192.168.74.0/24 -oN advanced_scan.txt

---

##  Scan Results

- Total Hosts Discovered: 3
- All scanned ports were either closed or filtered
- No open ports were detected

---

## Analysis

- Closed ports indicate that no services are actively running.
- Filtered ports suggest firewall protection is enabled.
- The system shows minimal attack surface exposure.

---

## Security Insights

- Open ports can expose services to unauthorized access.
- Firewall configuration plays a critical role in blocking suspicious traffic.
- Regular port scanning helps in identifying unintended service exposure.

---

## Key Concepts Learned

- Port Scanning
- TCP SYN Scan (Half-open scan)
- Network Reconnaissance
- Open vs Closed vs Filtered Ports
- Basic Firewall Behavior

---

## Interview Questions & Answers

### 1. What is an open port?
An open port is a network port that is actively accepting connections and has a service running behind it.

### 2. How does Nmap perform a TCP SYN scan?
Nmap sends a SYN packet. If it receives a SYN-ACK response, the port is open. If it receives RST, the port is closed. It does not complete the full handshake.

### 3. What risks are associated with open ports?
Unauthorized access, brute force attacks, service exploitation, and increased attack surface.

### 4. Difference between TCP and UDP scanning?
TCP is connection-based and reliable. UDP is connectionless and slower for detection.

### 5. How can open ports be secured?
By disabling unused services, enabling firewalls, using strong authentication, and regular updates.

### 6. What is a firewall’s role?
A firewall filters incoming and outgoing network traffic and blocks unauthorized access.

### 7. What is a port scan?
A technique used to identify open ports and running services on a system.

### 8. How does Wireshark complement port scanning?
Wireshark captures and analyzes packets to observe how Nmap communicates with target systems.

---

 Conclusion

This task helped in understanding basic network reconnaissance techniques and how to analyze network exposure using Nmap. Proper firewall configuration significantly reduces potential security risks.
