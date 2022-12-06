# Zscaler Zscaler Internet Access (ZIA) Microsoft Sentinel SIEM KQL Threat Hunting for a Phishing Attack

**Possible Phishing Attack detection:**
This use-case is helpful in case Microsoft Defender for 365 does not detect or quarantine a malicious phishing e-mail. Zscaler can see possible malicious phishing URLs based on website category and other metrics. By leveraging this information and a count of users visiting a flagged URL within one hour, we can identify a possible undetected phishing campaign. 

**Example:**

Let's say your organization is a target for a mass or targeted phishing campaign. This means multiple users can receive phishing mail. The picture below is an example malicious phishing e-mail. The "review recent activity" button does not direct you to a Microsoft page but to a malicious website through bit.ly URL shortening services. In this case, Microsoft M365 does not flag or quarantine this malicious mail:

![Example phishing e-mail](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/phishing-mail.png)

If the Zscaler ZIA endpoint agent is active on a system, it can keep track of all visited URLs. This way, we can create a KQL query to keep track of all links, which could be a security risk. In this case, when three or more employees click on the phishing bit.ly link - Sentinel will create an alert:

![ZIA phishing Sentinel SIEM](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/zscaler-phishing-siem.jpeg)

KQL query: https://github.com/krabelize/zscaler-sentinel-siem/blob/main/detect-phishing-attack.kql

GAP: users who clicked on the phishing link on their smartphones or tablets.

Goal: detect phishing campaigns which did not get blocked or detected by Microsoft 365 or Google Workspace.

# License
Berkeley Software Distribution (BSD)

# Author
[Jeroen van Kessel](https://twitter.com/jeroenvkessel) | [cryptsus.com](https://cryptsus.com) - we craft cyber security solutions
