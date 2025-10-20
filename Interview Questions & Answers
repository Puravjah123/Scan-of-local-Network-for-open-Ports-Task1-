BELOW ARE FEW QUESTIONS WITH ANSWER RELATE TO PORT SCANNING IN SYSYTEM :

1. What is an open port?

  Answer:
  An open port is a network endpoint that is actively accepting incoming connections from other devices. It represents a service or application running on a system that is listening for communications on a specific port number (0-65535).

  Well-known ports (0-1023): HTTP:80, SSH:22, FTP:21

  Registered ports (1024-49151): Assigned to specific services

  Dynamic ports (49152-65535): Ephemeral use

  Indicates an active service waiting for connections

2. How does Nmap perform a TCP SYN scan?

  Answer:
  A TCP SYN scan (half-open scanning) works through this process:

  bash
  # Nmap SYN Scan Command
  sudo nmap -sS 192.168.1.0/24
  Process:

  SYN Sent → Nmap sends TCP SYN packet to target port

  Response Analysis:

   SYN-ACK Received → Port is OPEN

   RST Received → Port is CLOSED

   No Response/ICMP Error → Port is FILTERED

  Connection Reset → Nmap sends RST packet instead of completing handshake

  Advantages: Stealthy, fast, efficient, less logging by IDS systems

3. What risks are associated with open ports?

  Answer:
  Critical Security Risks:

  Risk Level	Port Examples	Potential Threats
   High	445, 135-139, 3389	Ransomware, brute force, exploits
   Medium	22, 21, 23, 80	Credential theft, data interception
   Low	443, 53, 123	Service abuse, information leakage
  Specific Threats:

  Service Vulnerabilities: Buffer overflows, privilege escalation

  Unauthorized Access: Weak authentication, brute force attacks

  Information Disclosure: Banner grabbing reveals system details

  Malware Propagation: Worms spreading through vulnerable services

  Data Exfiltration: Unauthorized data transfer

4. Explain the difference between TCP and UDP scanning

  Answer:

  Aspect	TCP Scanning	UDP Scanning
  Protocol	Connection-oriented	Connectionless
  Reliability	High reliability	Unreliable delivery
  Scanning Method	SYN, Connect, ACK scans	UDP packet sending
  Response Analysis	Clear state responses	Often no response
  Speed	Fast	Slow (timeouts required)
  Accuracy	Highly accurate	Less reliable
  Commands	nmap -sS (SYN)	nmap -sU (UDP)
  Key Insight: TCP uses handshake-based communication while UDP relies on packet inference, making UDP scanning more challenging.

5. How can open ports be secured?

    Answer:
    Multi-Layer Security Approach:
    
     Network Level
    bash
    # Firewall example - block unnecessary ports
    sudo ufw deny 135,139,445/tcp
    sudo ufw allow 22/tcp  # Only allow required ports
     Host Level
    Close unused ports and disable unnecessary services
    
    Implement host-based firewalls
    
    Use port knocking for hidden services
    
    🔧 Service Hardening
    Regular security patches and updates
    
    Strong authentication mechanisms
    
    Encryption (SSL/TLS) implementation
    
    Change default ports for critical services
    
     Monitoring & Maintenance
    Regular vulnerability assessments
    
    Continuous network monitoring
    
    Security policy enforcement
    
    Employee security training

6. What is a firewall's role regarding ports?

    Answer:
    A firewall acts as a network traffic controller with these primary functions:
    
    Key Roles:
    
    Access Control → Allow/deny traffic based on rules
    
    Port Filtering → Block unnecessary ports
    
    Stateful Inspection → Track connection states
    
    Network Segmentation → Isolate network zones
    
    Threat Prevention → Block malicious traffic patterns
    
    Firewall Rules Example:
    
    bash
    # Sample iptables rules
    iptables -A INPUT -p tcp --dport 22 -j ACCEPT    # Allow SSH
    iptables -A INPUT -p tcp --dport 80 -j ACCEPT    # Allow HTTP
    iptables -A INPUT -p tcp --dport 443 -j ACCEPT   # Allow HTTPS
    iptables -A INPUT -j DROP                        # Deny everything else
7. What is a port scan and why do attackers perform it?

    Answer:
    
    Port Scan Definition:
    A port scan is a reconnaissance technique that probes a target system to discover open ports and available services.
    
    Attacker Motivations:
    
    Network Mapping → Identify active hosts and services
    
    Vulnerability Assessment → Find exploitable services
    
    Service Fingerprinting → Identify software versions
    
    Attack Planning → Prepare targeted exploits
    
    Security Posture Evaluation → Assess defense strength
    
    Common Scanning Techniques:
    
    TCP SYN Scan → Stealthy half-open scanning
    
    TCP Connect Scan → Complete connection establishment
    
    UDP Scan → Connectionless service discovery
    
    Version Detection → Service banner grabbing

8. How does Wireshark complement port scanning?

    Answer:
    Wireshark provides packet-level analysis that enhances port scanning:
    
    Complementary Functions:
    
    Nmap Scanning	Wireshark Analysis
    Identifies open ports	Shows actual packet exchange
    Discovers services	Analyzes protocol behavior
    Maps network topology	Detects network anomalies
    Fast reconnaissance	Deep packet inspection
    Practical Integration:
    
    bash
    # 1. Start Wireshark capture
    sudo wireshark &
    
    # 2. Perform Nmap scan
    sudo nmap -sS 192.168.1.0/24
    
    # 3. Analyze packets in Wireshark
    # - View SYN, SYN-ACK, RST packets
    # - Identify filtered ports behavior
    # - Detect intrusion detection systems
    Benefits:
    
    Validation → Verify scan results accuracy
    
    Troubleshooting → Identify network issues
    
    Education → Understand scanning mechanics
    
    Detection → Identify scanning patterns for defense

