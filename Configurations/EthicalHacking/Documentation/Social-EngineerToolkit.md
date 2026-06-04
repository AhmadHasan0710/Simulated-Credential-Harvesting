<h1>Social Engineering Toolkit (SET)</h1>

<h2>Purpose and Use Within This Lab</h2>

<p>
The Social Engineering Toolkit (SET) is used in this lab to create a credential harvesting attack through a cloned website. This demonstrates how attackers can trick users into entering sensitive information into a malicious page that appears legitimate. The captured data is then analyzed from a defensive perspective, as how can a network infrastructure configured properly, can detect and prevent any form of harvesting.
</p>

<ul>
<li>
SET can be utilized within any Linux distro, this lab specifically runs Ubuntu as its OS. The toolkit was launched and navigated through the following sequence: Sudo Setoolkit  → Social-Engineering Attacks → Website Attack Vectors → Credential Harvester Attack Method → Web Templates. The computer's IP address (192.168.254.23) was provided as the hosting server, and the Google login template was selected to replicate a familiar and trusted login page. The attack was then executed, hosting the phishing page and waiting for incoming connections.
</li>
</ul>

<h2>Phishing Email Delivered to Victim</h2>
<p>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/EmailReceived.png" alt="Phishing Email">
</p>

<p>
This is the email that in this lab, m3rcy1ok@gmail.com received. In real world cases, many things would change within this, the email/server the email is sent from, the formatting/legitimacy of this email, the domain & link, and so much more.
</p>

<h2>Victim Interaction (Clicking the Link)</h2>
<p>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/SETLinkVisited.png" alt="Victim Interacting">
</p>

<p>
When the victim clicks the link, the request is sent to the SET hosted server. If the connection is successful, the SET terminal will show an incoming connection from the target machine; typically a HTTP 200 code. If unsuccessful, the server may return an HTTP 403 error, indicating access was either denied, or the connection failed.
</p>

<h2>Credential Harvesting Page</h2>
<p>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/SETFakeWebpage.png" alt="Credential Harvesting Page">
</p>

<p>
The victim is presented with a cloned Google login page. In a real world scenario, this page would be hosted under a convincing domain name rather than a raw IP address to avoid suspicion. The victim then would enter their credentials, thinking the site is legit.
</p>

<h2>Post-Login Redirection</h2>
<p>
<a href="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/SETRedirect.png">View Screenshot</a>
</p>

<p>
After submitting credentials, the victim is redirected to the actual Google page itself. This helps reduce suspicion, as the user assumes a normal login flow rather than realizing their credentials were intercepted.
</p>

<h2>Captured Credentials in SET Terminal</h2>
<p>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/SETResults.png" alt="Captured Credentials">
</p>

<p>
The SET terminal displays the captured username and password in real time. This demonstrates how attackers can successfully harvest sensitive information without the victim being immediately aware of the compromise.
</p>
