# 📌 Findings – Wireshark Log Analysis  

# Overview

This PCAP contains network traffic from a web server targeted by a probe/scan from the IP address 139.199.184.166. The web server had been online for a few days before traffic was captured using dumpcap, revealing attempted connections and potential reconnaissance behavior.

# Key Observations

1. Evidence of External Scanning Activity

- The IP 139.199.184.166 showed high-frequency requests compared to other addresses in the dataset.

- Probing attempts suggest potential vulnerability enumeration on the web server.

2. Traffic Composition & Filtering Insights

- Majority of traffic consisted of web activity (HTTP), which is normal for an exposed web server.

- Filtering with !(tcp.port eq 80) revealed attempted connections to TCP ports 8080 and 8983, possibly trying to access alternative services or detect misconfigurations.

3. Sanitized Environment Details

- The internal web server had an IP of 10.12.25.101, while the external IP appeared as 128.199.64.235, simulated to resemble a Digital Ocean-hosted server.

- While the web server identity was sanitized, the scan behavior from 139.199.184.166 was legitimate and provides a real-world example of how attackers probe online services. 

