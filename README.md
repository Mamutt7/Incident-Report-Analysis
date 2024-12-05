# Incident Report Analysis

## Summary
The multimedia company experienced a **Distributed Denial of Service (DDoS)** attack that disrupted internal network services for two hours. The attack involved a flood of **ICMP packets**, which overwhelmed the network resources, preventing normal traffic from accessing critical services. 

The cause of the incident was traced to an **unconfigured firewall**, which allowed the malicious traffic to enter. The incident management team resolved the issue by blocking incoming ICMP packets, halting non-critical services, and restoring critical network functionality.

## NIST Cybersecurity Framework Analysis

### **1. Identify**
- **Type of Attack:** Distributed Denial of Service (DDoS) attack leveraging ICMP packet flooding.
- **Systems Impacted:** 
  - Internal network infrastructure.
  - Network services (critical and non-critical systems).
- **Cause:** Unconfigured firewall allowed ICMP packet flooding.

### **2. Protect**
To prevent similar attacks in the future:
- **Firewall Configuration:**  
  - Limit the rate of incoming ICMP packets.
  - Implement source IP address verification to filter spoofed IP packets.
- **Network Security Measures:**
  - Deploy IDS/IPS systems to detect and block suspicious ICMP traffic.
  - Provide employee training on network protocols and security configurations.
- **Policy Updates:**  
  - Regularly audit firewall rules.
  - Enforce best practices for network traffic monitoring and management.

### **3. Detect**
To enhance detection capabilities:
- Implement **network monitoring software** to identify unusual traffic patterns (e.g., abnormal ICMP packet floods).
- Use an **Intrusion Detection System (IDS)** to flag malicious activities based on suspicious ICMP traffic characteristics.
- Monitor logs from network devices to track:
  - Unauthorized access attempts.
  - Traffic from untrusted IPs.

### **4. Respond**
In the event of a future incident:
- **Containment:**
  - Block incoming malicious traffic by updating firewall rules dynamically.
  - Disconnect affected network segments if necessary.
- **Neutralization:**
  - Use IDS/IPS to terminate malicious connections.
  - Conduct IP address filtering to isolate attack sources.
- **Analysis:**
  - Log and analyze incident data to identify root causes and attack vectors.
  - Share findings with relevant stakeholders and adjust security measures.

### **5. Recover**
Steps to restore operations:
- **Immediate Recovery:**
  - Validate that network services and firewalls are functioning correctly.
  - Ensure all critical services are operational after incident resolution.
- **Data Recovery:**
  - Verify system integrity and cross-check for potential data corruption.
- **Future Preparedness:**
  - Document the incident for future reference.
  - Schedule regular incident response drills to improve team readiness.

---

## Reflections/Notes
This incident underscores the importance of:
1. Regular firewall audits to minimize vulnerabilities.
2. Using real-time monitoring and detection tools.
3. Having a comprehensive incident response plan for quick containment and recovery.

