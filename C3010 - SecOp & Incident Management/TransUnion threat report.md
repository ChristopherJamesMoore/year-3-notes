<b>Target: TransUnion</b> <i>credit reporting agency</i>
<h5>TransUnion attack</h5>
In July 2025 TransUnion, the credit reporting agency was attacked in a cybersecurity incident from a well known hacking group called the <i>ShinyHunters extortion group</i>. They exploited vulnerabilities within a Salesforce-linked application that affected >4.4million US customers. One of the reasons that this attack was so severe was that it was not discovered until 2 days after the attack took place. This slow response from TransUnion/ Salesforces cybersecurity team resulted in the attack being incredibly large. 
<h5>UNC6395 Drift OAuth abuse</h5>
Attacks like this to Salesforce have been conducted through compromised Drift OAuth tokens on a Salesforce application. The threat actors ran SOQL queries on Salesforce objects <i>(users, accounts, cases, etc..)</i>. This allowed them to exfiltrate sensitive credentials. The attack worked because OAuth tokens, unlike user sessions which expire quickly, do not often expire very quickly allowing long-term exposure.
<h5>Steps taken to prevent supply chain attacks</h5>
Over-permissive access was a driving force in this attacks success, applying the least amount of privileges to service accounts is one way to counter this flaw as knowing exactly what each account has access to ensures sensitive data is unable to be accessed wrongfully. 

Regularly checking for exposed secrets such as AWS keys, tokens, or passwords in the Salesforce schema and other data records. This will greatly help limit attackers from gaining access to sensitive systems through these secrets.








