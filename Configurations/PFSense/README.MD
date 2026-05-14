<h1>pfSense Configuration Files</h1>

<p>
This directory contains structured configuration files for the pfSense firewall within this network infrastructure.
</p>

<p>
The <b>liveconfig.xml</b> file represents the complete, active configuration used by the system. It contains the full set of operational settings required for the firewall to function, including interfaces, VLAN assignments, firewall rules, NAT, and additional configurations.
</p>

<p>
The additional XML files in this directory are not intended for direct deployment. Instead, they are used to organize and break down the main configuration into logical sections such as routing, firewall rules, DNS, and NAT. This separation is meant to improve readability, maintainability, and overall clarity of the network design.
</p>