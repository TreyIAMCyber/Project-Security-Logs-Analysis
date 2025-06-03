# 📌 Findings – Wireshark Log Analysis  

## 🔹 Key Observations  
1. **Common Traffic Patterns**  
   - Majority of packets involved **HTTP and HTTPS traffic**, indicating typical web browsing activity.  
   - DNS queries resolved multiple domains, showing interactions with external servers.  

2. **Filtering & Analysis Approach**  
   - Used `http.request` to **identify websites accessed**.  
   - Applied `tls.handshake.type == 1` to **track encrypted connections**.  
   - Analyzed IP addresses to **map communication flow** between devices.  

3. **Potential Security Flags**  
   - Noticed **high-frequency requests** to external IPs—could indicate automation or unusual behavior.  
   - Some packets contained **unexpected protocols** (FTP & Telnet traffic)—possible security risk?  
   - Certain DNS queries resolved **questionable domains**, worth deeper analysis.  

