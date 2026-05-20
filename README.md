# network-traffic-analysis-incident
Cybersecurity Incident Report: Network Traffic Analysis
Overview

This project analyzes a network incident involving DNS resolution failure for the domain yummyrecipesforme.com using tcpdump logs. The investigation focuses on identifying the root cause of connectivity issues affecting users attempting to access the website.

Part 1: Summary of the Problem

Analysis of the tcpdump logs indicates a failure in DNS resolution. The client device attempted to resolve the domain name yummyrecipesforme.com using the DNS protocol over UDP (port 53). However, the DNS server responded with ICMP error messages indicating that UDP port 53 was unreachable.

The logs show repeated UDP DNS query attempts followed by ICMP error responses stating “udp port 53 unreachable,” which suggests that the DNS service is not properly responding to requests.

Additionally, the presence of DNS query flags (such as the “A?” record request) confirms that standard DNS resolution processes were initiated but not successfully completed.

Based on this evidence, the issue appears to be a failure in DNS communication, likely due to a server-side or network path issue.

Part 2: Analysis and Possible Causes

The incident occurred at approximately 1:24 p.m. when users reported being unable to access the website yummyrecipesforme.com, receiving the error message “destination port unreachable.”

Packet analysis using tcpdump confirmed that DNS queries sent to port 53 were not receiving valid responses.

Possible Causes:
DNS server outage or service failure
Firewall rules blocking UDP port 53 traffic
Misconfiguration in DNS service settings
Potential Denial-of-Service (DoS) attack targeting DNS infrastructure
Next Steps:
Verify DNS server operational status
Check firewall rules for UDP port 53
Review system logs for service crashes or overload
Monitor for abnormal traffic patterns indicating a potential attack
Key Skills Demonstrated
DNS protocol analysis
Network traffic investigation (tcpdump)
Incident documentation and reporting
Cybersecurity troubleshooting workflow
What I fixed (important)
Made tone more “incident report / SOC style” (less school wording like “using tcpdump logs” repetition)
Cleaned sentence flow (more professional readability)
Reduced slightly repetitive phrasing
Tightened security wording (“server-side or network path issue” is more industry standard)
Improved consistency in formatting (recruiters care about this more than you think)
