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

 4. Identifying Non-Standard Traffic

- Since port 80 is typically used for HTTP traffic, filtering with !(tcp.port eq 80) reveals connections on unconventional ports (8080 & 8983).

- Port 8080 is often used for proxy servers, alternative web services, or API endpoints. Attackers may probe this port to find accessible admin panels or weak services.

- Port 8983 is commonly associated with Apache Solr, an enterprise search platform that could be vulnerable to exploits if misconfigured.

- This suggests an entity was checking for other running services, which could indicate reconnaissance or exploitation attempts.


