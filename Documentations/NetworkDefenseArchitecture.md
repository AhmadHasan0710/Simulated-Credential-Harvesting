<h1>Network Defense Architecture</h1>

<h2>Overview and Purpose</h2>
<p>
This section outlines how the network architecture was designed within this lab, to simulate a layered security approach, combining multiple tools and configurations to monitor, filter, and protect network traffic. While the attack methodology demonstrates how phishing attacks are executed, this section highlights how such threats can be detected, analyzed, and mitigated within a controlled environment.
</p>

<p>
At the core of this architecture is PFSense, which functions as the primary firewall and network router. Additional tools such as Pi-hole, pfBlockerNG, Suricata, Zeek, and Darkstat are integrated to provide enhanced visibility, filtering, and intrusion detection capabilities.
</p>

<h2>PFSense Configuration and Role</h2>
<p>
PFSense serves as the central component of the network, managing traffic flow between VLANs and enforcing security policies. It is responsible for routing, firewall enforcement, network segmentation, and much more.
</p>

<ul>
<li><b>DHCP Configuration:</b> PFSense provides DHCP services to dynamically assign IP addresses to devices across different VLANs, ensuring proper network segmentation and management.</li>

<li><b>Firewall Configuration:</b> Custom firewall rules were implemented to control traffic between VLANs, restricting unauthorized access while allowing necessary communication for lab functionality.</li>

<li><b>Interfaces Configuration:</b> Multiple interfaces were configured to separate network segments, including attacker, victim, and server environments. This segmentation helps simulate real world enterprise networks.</li>

<li><b>NAT Configuration:</b> NAT was configured to allow internal devices to access external networks while masking internal IP addresses, providing an additional layer of security.</li>

<li><b>VLAN Configuration:</b> VLANs were used to logically separate different parts of the lab environment. This ensures that traffic can be controlled and monitored between segments, which is critical for both attack simulation and defense analysis.</li>
</ul>

<h2>Pi-hole (DNS Filtering)</h2>
<p>
Pi-hole was deployed on a separate Ubuntu server and configured to use DNS over HTTPS (DoH). It functions as a network wide ad blocker and DNS filter, preventing connections to known malicious or unwanted domains. This adds a proactive layer of defense by blocking potentially harmful requests before they reach their destination.
</p>

<h2>pfBlockerNG (IP & DNS Blocking)</h2>
<p>
pfBlockerNG, integrated within PFSense, was used to block malicious IP addresses and domains based on threat intelligence feeds. It enhances PFSense’s native firewall capabilities by automatically updating blocklists and preventing communication with known malicious sources.
</p>

<h2>Suricata (Intrusion Detection & Prevention System)</h2>
<p>
Suricata was configured on PFSense as an IDS/IPS to monitor network traffic in real time. It analyzes packets for suspicious patterns and known attack signatures, generating alerts when potential threats are detected. This is particularly useful for identifying phishing-related traffic and abnormal behavior during the attack simulation.
</p>

<h2>Zeek (Network Traffic Analysis)</h2>
<p>
Zeek was used as a network analysis framework to provide deeper insight into network activity. Unlike traditional IDS tools, Zeek focuses on logging and analyzing traffic behavior, allowing for detailed investigation of connections, protocols, and potential anomalies.
</p>

<h2>Darkstat (Traffic Monitoring)</h2>
<p>
Darkstat was used to provide lightweight, real time monitoring of network traffic. It offers a visual representation of bandwidth usage, active connections, and overall network activity; helping to quickly identify unusual spikes or patterns during the lab.
</p>

<h2>Conclusion</h2>
<p>
This network defense architecture demonstrates how multiple security tools can be integrated to protect against many malicious attacks. By combining firewall enforcement, DNS filtering, intrusion detection, and traffic analysis; the lab provides a comprehensive view of both offensive and defensive cybersecurity & networking practices.
</p>
