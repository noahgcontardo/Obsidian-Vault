Alert 1

Who
- Source: User on internal host with IP `10.1.3.129`
- Destination: External host at IP `178.92.53.38`
- User/Process: User manually typed the URL.

2. When

- Timestamp of First Alert: 24 January 2025, 21:50
- Timestamp of Second Alert: 24 January 2025, 21:52

3. What

- Incident Description:
- The first alert was triggered by a mistyped URL (`googl.com`), which was flagged by the system as a potential typosquatting attack. As a result, the connection was blocked.
- The user corrected the URL two minutes later, typing the valid address `google.com`. This connection attempt was not flagged.

4. Where

- Source IP: `10.1.3.129` (Internal Network)
- Destination IP: `178.92.53.38` (External Host)
- Application: Web-browsing (via TCP)
- Rule Applied: Allow-Internet (For successful web connection to google.com)

5. Why

- Why did the alert trigger? — The first alert was caused by a mistyped URL (`googl.com`), which our system flagged as a possible ****typosquatting attack**** due to the similarity to a well-known domain (google.com).
- Why was the action taken? — The system blocked the action to protect against potential malicious typosquatting, which involves creating look-alike domains to deceive users into visiting fake websites for phishing or malware distribution.
- Why was the second connection allowed? — The user correctly typed yahoo.com, which is a legitimate URL, and the connection was allowed by the firewall rule `Allow-Internet`.
- Why was this a false positive? — 