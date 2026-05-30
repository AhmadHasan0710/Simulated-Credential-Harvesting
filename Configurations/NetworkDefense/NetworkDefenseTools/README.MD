# Network Defense Tools

This folder specifically contains all Network Defense Tools utilized within this Lab, in partnership with the already established PFSense Firewall & Router.

While pfSense handles core network controls such as routing, VLANs, firewall rules, and NAT, the tools in this section are responsible for monitoring, detection, and analysis within the network.

These tools work together with the firewall to provide a more deep visibility into all network activity, and help identify potential threats in real time.


Included in this section are configurations and setups for tools such as:

<ul>
<li>Zeek (network traffic analysis and logging)</li>
<li>Suricata (IDS/IPS for threat detection and alerting)</li>
<li>Pi-hole with DNS over HTTPS (secure DNS filtering and blocking)</li>
<li>pfBlockerNG-devel (IP and DNS-based filtering integrated with pfSense)</li>
<li>Darkstat (real-time network traffic monitoring)</li>
</ul>

These tools do not replace the firewall, but instead enhance it by providing detailed insight into traffic, detecting suspicious behavior, and supporting defensive analysis within the environment.
