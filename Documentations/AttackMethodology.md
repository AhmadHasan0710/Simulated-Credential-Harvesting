<h1>Attack Methodology</h1>

<h2>Overview</h2>
<p>
This section outlines the complete attack methodology used in this lab; combining both GoPhish and SET to simulate real world credential harvesting attacks. The process demonstrates how an attacker can plan, deliver, and execute a phishing campaign, all to capture sensitive user credentials.
</p>

<h2>Step by Step Attack Process</h2>

<h3>1. Environment Preparation</h3>
<p>
The lab environment was prepared by configuring both attacker and victim machines to be within the same network initially (Management & Guest Networks). The attacker machine hosted both GoPhish and SET, while the victim machine was used to simulate user interaction with the phishing email and malicious website.
</p>

<h3>2. Phishing Infrastructure Configuration (GoPhish)</h3>
<p>
GoPhish was configured to handle email delivery and campaign management. This included setting up the admin server, phishing server, landing & sending profile, and email sending profile. The phishing template was created to mimic a legitimate security alert, increasing the likelihood of user interaction.
</p>

<h3>3. Campaign Creation and Deployment</h3>
<p>
A campaign was created within GoPhish, targeting selected email addresses. The phishing email contained a link directing the victim to the malicious page.
</p>

<h3>4. Credential Harvesting Setup</h3>
<p>
SET was used to create a cloned login page. Through its menu-driven interface, the following options were selected: Social-Engineering Attacks → Website Attack Vectors → Credential Harvester → Web Templates. The attacker’s IP address was used to host the page, and a Google login template was chosen to replicate a familiar interface.
</p>

<h3>5. Email Delivery and Victim Interaction</h3>
<p>
The phishing email was successfully delivered to the victim. Upon receiving the message, the victim clicked the embedded link, initiating a connection to the attacker’s hosted server.
</p>

<h3>6. Connection Handling and Server Response</h3>
<p>
When the victim accessed the link, the SET server processed the request. A successful connection resulted in the phishing page being displayed. In cases where the connection failed, the server returned an HTTP 403 error, indicating access was denied or the request could not be fulfilled.
</p>

<h3>7. Credential Submission</h3>
<p>
The victim was presented with a cloned login page and prompted to enter their credentials. In real world scenario, attackers would use more legitimate looking domain names, rather than a raw IP address, to increase the credibility of the site.
</p>

<h3>8. Data Capture and Logging</h3>
<p>
Once the victim submitted their credentials, SET captured and displayed the information in real time within the terminal. This demonstrated how sensitive data can be intercepted without the user’s awareness.
</p>

<h3>9. Post-Submission Redirection</h3>
<p>
After credential submission, the victim was redirected to the legitimate Google page. This step helps maintain the illusion of a normal login process, reducing the likelihood that the victim suspecting any malicious activity.
</p>

<h2>Conclusion</h2>
<p>
This attack methodology demonstrates the full lifecycle of a phishing campaign, from initial setup to credential capture. By combining GoPhish for delivery and SET for exploitation, the lab provides a comprehensive understanding of how social engineering attacks are executed and how they can be mitigated.
</p>
