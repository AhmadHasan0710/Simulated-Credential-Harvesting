<h1>Credential Harvesting Results</h1>

<h2>Overview</h2>
<p>
This section presents the results of the credential harvesting simulation, that was done using Gophish and set. The goal of this phase was to evaluate the effectiveness of phishing techniques, while also measuring user interaction within a controlled lab environment.
</p>

<h2>Attack Execution Flow</h2>
<p>
The phishing campaign was successfully deployed using Gophish, with combination with set. Emails were delivered to the target using my Mailgun sandbox environment, simulating a realistic phishing attempt.
</p>

<ul>
<li><b>Email Delivery:</b> The phishing email was successfully sent to the victim without delivery issues.</li>
<li><b>User Interaction:</b> The victim opened the email and clicked on the embedded link.</li>
<li><b>Redirection:</b> The link directed the victim to a phishing page hosted via SET, designed to replicate a legitimate login portal.</li>
<li><b>Phishing Page Hosting:</b> The malicious page was hosted locally within the lab environment and accessible over HTTP.</li>
</ul>

<h2>Detection and Prevention</h2>
<p>
As the victim attempted to access the phishing page, the network defense actively monitoring the connection; with tools such as Suricata and pfBlockerNG-Devel, analyzing the traffic in real time.
</p>

<ul>
<li><b>Suspicious Indicators:</b> The destination IP address as the URL, lack of SSL/TLS certification, and unusual traffic patterns were identified as potential threats.</li>
<li><b>Intrusion Detection:</b> Suricata generated alerts based on these indicators, flagging the connection as suspicious.</li>
<li><b>Intrusion Prevention:</b> Operating in IPS mode, Suricata blocked the connection before the phishing page could fully load.</li>
<li><b>Network Enforcement:</b> The malicious IP address was effectively blocked at the firewall level, preventing further connectoin between the victim and the phishing server.</li>
</ul>

<h2>Analysis</h2>
<p>
The results demonstrate a successful end to end simulation, of not only a phishing attack, but also followed by an effective detection and prevention system. While the phishing email and redirection process functioned as intended, the defensive systems jumped in before any credentials could be harvested.
</p>

<p>
This highlights the importance of layered security. Even when a user interacts with a phishing attempt, properly configured intrusion detection and prevention systems can mitigate the risk before compromise occurs.
</p>

<h2>Conclusion</h2>
<p>
This lab successfully showcased both offensive and defensive cybersecurity and networking techniques. The attack phase demonstrated how easily users can be led to malicious sites, while the defense phase proved that tools such as Suricata and PFBlockerNG-Devel can detect and block threats in real time, ultimately preventing credential compromise.
</p>
