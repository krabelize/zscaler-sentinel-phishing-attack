# Zscaler Zscaler Internet Access (ZIA) Microsoft Sentinel SIEM KQL Threat Hunting for a Phishing Attack

**Possible Phishing Attack detection:**
This use-case is useful in case Microsoft Defender for 365 does not detect or quarentine a malicious phishing e-mail. Zscaler can detect possible malicious phishing URL's based on website catagory and other metrics. By leveraging this information, together with a count of users visiting a flagged URL, we can identify a possible undetected phishing campaign. 

KQL query: https://github.com/krabelize/zscaler-sentinel-siem/blob/main/detect-phishing-attack.kql

**Example:**

Let's say your organization is a target for a mass or targetted phishing campaign. This means multiple users can receive a phishing mail. The picture below is an example malicious phishing e-mail. The "review recent activity" button does not direct you to a Microsoft page, but to a malicious website through bit.ly URL shortening services. In this case, Microsoft M365 did not flag or quarentine this malicious mail.

![Example phishing e-mail](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/phishing-mail.png)

If the Zscaler ZIA endpoint agent is active, it is able to keep track of all visited URL's. This way, we can createa a KQL query to keep track of all links which could be a security risk. In this case, when three or more employees clicked on the phishing bit.ly link - Sentinel will create an alert:

![ZIA phishing Sentinel SIEM](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/zscaler-phishing-siem.jpeg)

# License
Berkeley Software Distribution (BSD)

# Author
[Jeroen van Kessel](https://twitter.com/jeroenvkessel) | [cryptsus.com](https://cryptsus.com) - we craft cyber security solutions
