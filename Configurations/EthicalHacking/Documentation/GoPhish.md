<h1>GoPhish Configuration</h1>

<p>
This file explains the overall configuration choices, as well as the intended purpose behind using GoPhish within this lab. The goal was to simulate a realistic phishing campaign, in a controlled environment, in order for defensive analysis.
</p>

<h2>Sending Profile</h2>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/GophishSendingProfile.png" alt="Sending Profile">

<p>
The sending profile was configured using Mailgun as the SMTP provider. Other SMTP providers could've been used, but Mailgun's free sandbox provider made it much more efficent. This domain limited the emails it can send to by only allowing approved emails.
</p>

<p>
In real-world scenarios, a legitimate domain and more advanced configured SMTP server, would be used to increase the campaign's realism and avoid any form of detection.
</p>

<h2>Landing Page</h2>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/GophishLandingProfile.png" alt="Landing Page">

<p>
The landing page is configured to only redirect users to the SET server.
</p>

<p>
Gophish as a whole, also attempts to handle any form of credential harvesting; this specific landing page essentially takes away from that, and forces SET's server to do the credential harvesting, while Gophish is reserved to only payload delivery.
</p>

<h2>Email Template</h2>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/GophishEmailTemplate.png" alt="Email Template">

<p>
A general security alert email was created, warning users of a possible unknown password change, and urging the specific victim it sends to, to take action
</p>

<ul>
<li>Creates urgency</li>
<li>Applies to any victim it's sent to</li>
<li>Includes a clickable link</li>
</ul>

<p>
The link specifically, is configured later within the campaign section.
</p>

<h2>Users and Groups</h2>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/GophishUser%26Groups.png" alt="Users and Groups">

<p>
Users and groups define who receives the phishing emails.
</p>

<p>
Only test emails were added due to Mailgun sandbox restrictions, which require approved recipients. In real world Scenarios, much larger groups of individuals would be at use, either imported online or through other
</p>


<h2>Campaign</h2>
<img src="https://github.com/AhmadHasan0710/Simulated-Credential-Harvesting/blob/main/Screenshots/EthicalHackingScreenshots/GophishCampaign.png" alt="Campaign">

<p>
The campaign connects all configured components together:
</p>

<ul>
<li>Sending Profile</li>
<li>Landing Page</li>
<li>User Groups</li>
<li>Email Template</li>
</ul>

<p>
The URL/IP used within the email is:
</p>

<p><b>http://192.168.254.23:8080</b></p>

<p>
Port 8080 is used by the GoPhish server, and the IP represents the internal lab system. This works with the landing page redirect, where the user clicks the link, is tracked by GoPhish, and then redirected to SET by the Landing Page's configuration
</p>

<p>
In real world scenarios, IP-based links are avoided, due to the fact that they're easily flagged. Instead, legitimate domains are used, to increase the overall look of it.
</p>

<h2>Continuation</h2>

<p>After the payload is successfully sent to everyone's email specified via users & group, the results are shown via where SET is being ran. This is, of course after credentials have been inputted within the link SET provides us.</p>