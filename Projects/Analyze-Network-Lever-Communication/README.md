# Activity: Analyze DNS and ICMP Traffic

Analyze DNS and ICMP traffic in transit using data from a network protocol analyzer tool. You will identify which network protocol was utilized in the assessment of the cybersecurity incident.

At the internet layer of the TCP/IP model, the IP formats data packets into IP datagrams. The information provided in the datagram of an IP packet can provide security analysts with insight into suspicious data packets in transit.

Knowing how to identify potentially malicious traffic on a network can help cybersecurity analysts assess security risks on a network and reinforce network security.

## Scenario

Review the scenario below. Then complete the step-by-step instructions.

You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of clients reported that they were not able to access the client company website www.yummyrecipesforme.com, and saw the error "destination port unreachable" after waiting for the page to load.

You were tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you attempt to visit the website and you also receive the error "destination port unreachable." To troubleshoot the issue, you load your network analyzer tool, Wireshark, and attempt to load the webpage again. To load the webpage, your browser sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol. Your browser then uses this IP address as the destination IP for sending an HTTPS request to the web server to display the webpage. The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: "udp port 53 unreachable."

 ![image](https://github.com/user-attachments/assets/b60f5de1-a23f-49df-bc11-4ce27599df92)


 The image you provided appears to show a series of network traffic logs, likely captured using a tool like Wireshark or tcpdump. The logs detail a sequence of DNS requests and ICMP responses, indicating potential issues with the network or server. Let's break down the information:

### **Summary of the Traffic:**
1. **DNS Queries (UDP):**
   - The client at IP `192.51.100.15` is sending DNS queries to the DNS server at IP `203.0.113.2`. The queries are for the domain `yummyrecipesforme.com`, specifically asking for an A record (which is used to map a domain to an IPv4 address).

2. **ICMP Responses:**
   - In response to these DNS queries, the server at `203.0.113.2` is returning ICMP "Destination Unreachable" messages. Specifically, the message indicates "udp port 53 unreachable."

### **Analysis:**

#### **1. DNS Queries:**
   - The client (`192.51.100.15`) is attempting to resolve the domain name `yummyrecipesforme.com` by querying the DNS server (`203.0.113.2`) on port 53, which is the standard port for DNS queries over UDP.

#### **2. ICMP "Destination Unreachable" Responses:**
   - The ICMP responses from `203.0.113.2` indicate that the DNS server is unable to process the request because the specific service (UDP port 53) is unreachable.
   - Possible reasons for the ICMP messages:
     - **The DNS server is down** or not listening on UDP port 53.
     - **Firewall or security software** might be blocking access to UDP port 53 on the DNS server.
     - **DNS service configuration issues**: The DNS service on the server may not be properly configured or might have crashed.

#### **3. Implications:**
   - The client is unable to resolve the domain `yummyrecipesforme.com`, leading to connection failures. Users trying to access this domain would likely experience issues such as not being able to load the website, potentially seeing errors like "DNS server not responding" or "Unable to resolve the domain."

#### **4. Repeated Attempts:**
   - The client retries the DNS query several times, and each time, it receives the same ICMP "Destination Unreachable" response. This suggests that the issue is persistent and not intermittent.

### **Conclusion:**

The network traffic logs indicate that the DNS server at `203.0.113.2` is not functioning correctly, at least for UDP requests on port 53. This is preventing the client from resolving the domain `yummyrecipesforme.com`, resulting in failed attempts to connect to the website.

### **Possible Next Steps:**
- **Check the DNS server (`203.0.113.2`)**: Ensure that the DNS service is running and correctly configured to handle requests on UDP port 53.
- **Inspect Firewall/Security Rules**: Verify that there are no firewall rules or security settings blocking UDP traffic on port 53 to/from the DNS server.
- **Troubleshoot DNS Service**: Look for potential issues such as service crashes, misconfigurations, or resource constraints that might be causing the DNS service to be unreachable.

This analysis can help in diagnosing and resolving the network issue, ensuring that the domain name resolution process works as expected.
