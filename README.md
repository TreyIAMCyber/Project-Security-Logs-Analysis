# Basic Log Analysis with Wireshark 🦈🔬

 Overview: This homelab is designed to introduce myself to network traffic analysis in a simple, manageable way. I'll use Wireshark to examine a sample PCAP file, apply basic 
 filters, and identify key patterns in network logs. This foundational approach will help to build confidence before expanding into more complex cybersecurity workflows.
 
# 🔑Key Objectives:

1. Familiarization with Wireshark – Learn the UI, explore captured packets, and understand basic network protocols.

2. Apply Simple Filters – Use Wireshark’s filtering system to focus on HTTP/HTTPS requests, IP addresses, and ports.

3. Identify Key Traffic Patterns – Determine which IPs are communicating, which websites are accessed, and how data flows.

4. Document Findings – Write a brief summary of observations, practicing structured analysis for future security investigations.

# 🛠️Tech Stack/Tools Used: 

Wireshark – The primary tool for capturing and analyzing network traffic from your sample PCAP file.

Your Computer (Windows/Linux/macOS) – No need for virtual machines or complex setups yet.

Sample PCAP File – Download a recorded network traffic file for analysis instead of live packet capture

# 🎣Conclusion/Takeaways:

Basic Log Analysis with Wireshark

This project was all about getting hands-on with network traffic analysis—no crazy setups, just me, Wireshark, and a sample PCAP file. The goal was simple: get familiar with packet structures, apply filters, and start thinking like an analyst without drowning in overly complex tools.

What I Found Interesting

Network Traffic is Messy – A single capture file is packed with thousands of packets, and finding meaningful data requires knowing what to filter and where to look.

Filtering is Everything – Instead of sifting through a massive traffic dump, Wireshark's filters help zero in on specific protocols like HTTP requests or TLS handshakes.

Patterns Matter – Not every packet is interesting on its own, but noticing patterns in communication (who's talking to whom, what services are used) makes a difference.

# 🏆Why This Matters for SOC Work

Filtering logs efficiently = reducing noise and focusing on security-relevant data.

Recognizing normal vs. abnormal traffic = essential for detecting threats.

Documenting findings clearly = turning raw packet data into actionable security insights.

This first step was about building a solid foundation before jumping into automation or complex setups. The plan? Keep refining log analysis skills and eventually start integrating Python scripts to extract key security indicators automatically.

