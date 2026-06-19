<h1>Troubleshooting</h1>

<h2>Overview</h2>
<p>
This section outlines all the common issues I encountered during the setup, as well as the ending of this lab; along with their causes and solutions.
</p>

<h2>Gophish Issues </h2>
<p><b>Issue:</b> Emails were more often then not, reaching spam inboxes.</p>
<p><b>Cause:</b> Since Mailgun was in sandbox mode, made the configurations plus accessibility extremley limited.</p>
<p><b>Solution:</b></p>
<ul>
<li>Verify SMTP credentials</li>
<li>Ensure recipient emails are either authorized in sandbox mode, or dont use sandbox mdoe</li>
<li>Confirm domain verification status</li>
</ul>

<h2>Redirect & Tracking Issues</h2>
<p><b>Issue:</b> Campaign links with <code>?rid=</code> did not properly redirect.</p>
<p><b>Cause:</b> Misconfigured redirect settings between Gophish and SET.</p>
<p><b>Cause:</b> Kept redirecting to a misconfigured link</p>
<p><b>Solution:</b></p>
<ul>
<li>Correctly configure the redirect URL within Gophish</li>
<li>Ensure SET server is reachable, as well as configured correctly</li>
<li>Test links manually before launching any ampaign</li>
</ul>

<h2>Phishing Page Not Loading</h2>
<p><b>Issue:</b> Users unable to access cloned login page.</p>
<p><b>Cause:</b> Incorrect binding or firewall restrictions.</p>
<p><b>Solution:</b></p>
<ul>
<li>Bind SET to <code>0.0.0.0</code></li>
<li>Open required ports on pfSense (8080)</li>
<li>Verify connectivity via browser</li>
</ul>

<h2>Firewall / IDS Blocking Traffic</h2>
<p><b>Issue:</b> Traffic blocked between Gophish, SET, or users.</p>
<p><b>Cause:</b> pfSense rules, Suricata IPS, and pfBlockerNG kept interfering.</p>
<p><b>Solution:</b></p>
<ul>
<li>Temporarily disable blocking features</li>
<li>Add pass rules for specific lab traffic</li>
<li>made exceptions within the firewall</li>
</ul>

<h2>TLS and Certificate Errors</h2>
<p><b>Issue:</b> Browser warnings and/or failed HTTPS connections.</p>
<p><b>Cause:</b> Self signed or missing certificates.</p>
<p><b>Solution:</b></p>
<ul>
<li>Use HTTP for internal lab testing</li>
<li>Configure TLS properly if required</li>
<li>Ensure consistent protocol usage</li>
</ul>

<h2>Summary</h2>
<p>
Most issues encountered were related to network configuration, service accessibility, and external email provider limitations. Systematic testing at each stage helped figure out and resolve problems efficiently.
</p>
