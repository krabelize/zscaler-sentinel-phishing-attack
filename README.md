# Zscaler Zscaler Internet Access (ZIA) Microsoft Sentinel SIEM KQL Threat Hunting for a Phishing Attack

**Possible Phishing Attack detection:**
This use-case is useful in case Microsoft Defender for 365 does not detect or quarentine a malicious phishing e-mail. Zscaler can detect possible malicious phishing URL's based on website catagory and other metrics. By leveraging this information, together with a count of users visiting a flagged URL, we can identify a possible undetected phishing campaign. 

KQL query: https://github.com/krabelize/zscaler-sentinel-siem/blob/main/detect-phishing-attack.kql

**Example:**

![Example phishing e-mail](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/phishing-mail.png)

In case three or more employees, clicked on the phishing bit.ly link - Zscaler will log this and alert on this:

![ZIA phishing Sentinel SIEM](https://github.com/krabelize/zscaler-sentinel-siem/blob/main/zscaler-phishing-siem.jpeg)

# License
Berkeley Software Distribution (BSD)

# Author
[Jeroen van Kessel](https://twitter.com/jeroenvkessel) | [cryptsus.com](https://cryptsus.com) - we craft cyber security solutions
