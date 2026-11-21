# Email Tracking Pixel Simulation & Header Analysis 🎯

In this module, I practiced analyzing a suspicious email and wrote a custom Python script to simulate a "Tracking Pixel" to see if a victim opens the email.

## 1. Email Header Analysis
I analyzed a `.eml` file to check for spoofing indicators.
*   **SPF, DKIM, DMARC:** Checked the authentication results.
*   **Suspicious Indicators:** Noticed a mismatch between the `From` address and the `Reply-To` address, which is a common phishing tactic.

## 2. The Tracking Pixel Setup
I created a simple HTML email (`sample.eml`) that contains a 1x1 hidden image tag pointing to my local machine:
`<img src="http://localhost/Red-Circle-Transparent.png" width="1" height="1" alt="" />`

When the victim opens the email, the email client downloads the image, sending a request to my server.

## 3. Python Logging Server
I wrote a Python script using `http.server` to act as the tracking server. It logs the client's IP address, the timestamp, and their **User-Agent** (which tells us what email client they are using).

👉 **[Click here to view the Python Code (emailLOG.py)](./emailLOG.py)**

## 4. The Results
I started the server and opened the `sample.eml` file in an email client. The terminal successfully captured the request!

```text
Starting server...
127.0.0.1 - - [19/Nov/2026 14:19:45] "GET /Red-Circle-Transparent.png HTTP/1.1" 200 - User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:160.0) Gecko/20100101 Thunderbird/160.0
