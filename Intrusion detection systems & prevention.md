<h3>The CIA triad</h3>
- Confidentiality
	- Sensitive data is accessed by authorised personnel only
- Integrity
	- Protection against unauthorised modification
- Availability
	- Data is accessible by authorised personnel when needed

<b>Confidentiality</b>
Protecting sensitive data against unauthorised access is achieved using:
- Encryption
- Access controls and role-based permissions
- 2FA/ MFA
This data could include personal data such as customer records, bank details, employee information, or even IP. 

<b>Integrity</b>
Ensuring data is reliable, consistent, and protected against unauthorised changes. Integrity is incredibly important in sectors like:
- Healthcare
- Finance
- E-commerce
Checksums, version control, and audit logs maintain integrity throughout data's life cycle.

<b>Availability</b>
Ensuring authorised users can access information and systems as needed. Downtime in systems can occur from:
- Power outages
- Hardware/ software failures
- Ransomware attacks or DDoS attacks
Critical systems can be duplicated to create consistent uptime and redundancy, as well as keeping regular backups, using automatic failover, and monitoring performance to catch potential issues early.

<h3>Intrusion attempt</h3>
Intrusion attempts are deliberate unauthorised attempts to access senitive information (<i>confidentiality</i>), manipulate information (<i>integrity</i>), or render a system unreliable or unusable (<i>availability</i>).

<b>Brief history</b>
- 1980
	- Automated audit trail review
	- Automated collection of information for review by security personnel
	- Reduction of irrelevant records
- 1987
	- Generic intrusion detection model 
<h3>Dorothy Denning</h3>
<b>Generic intrusion model</b>
![[Pasted image 20250929110708.png]]
<h3>What is an IDS?</h3>
Intrusion detection systems are security tools designed to monitor network traffic and system activities for signs of potential attacks and unauthorised access. An example of a well-known IDS is snort.
<i>Access control</i> - Restrict access to objects according to access rights of the subject
<i>Identification & authentication</i> - Positively identify objects and subjects to the system
<i>Encryption</i> - Obscure the content of information, eliminating the possibility of surveillance by unauthorised parties
<i>Firewall</i> - Enforce a network-level access control policy

<i><font color="grey">An IDS can be thought of as a security camera monitoring the door that gives access to an important room</i></font>

<b>IDS classification</b>
IDS can be classified according to three factors:
- The source from which they collect data and analysis
- The detection mechanism by which the collected data is then analysed in order to detect potential intrusions
- The response mechanisms which are triggered as a result of generated alerts
![[Pasted image 20250929113541.png]]

<b>Types of IDSs</i>
<b><i><u>Host</b></i></u>
Utilises two types of information sources, operating system audit trails, and system logs
<b><i><u>Network</b></i></u>
Examines network traffic. Often consists of single purpose sensors that run in stealth mode
<b><i><u>Hybrid</b></i></u>
Combines two or more of the sources above

<b>Host-based IDS</b>
<u>Advantages</u>
- Not affected by switched networks
- Not affected by encryption
- Can determine the outcome of an attack
- Detection more reliable and precise, due to the vast amount of information they can collect from a system
<u>Disadvantage</u>
- Takes up resources on the system
- Cannot detect attacks that target an entire network, e.g., network scans
- May be tarted and disabled as part of the attack
- Large number of monitored hosts can be harder to manage

<b>Network-based IDS</b>
<u>Advantages</u>
- Can monitor many hosts
- Has little impact upon existing network structure
- Can monitor different OSs
- Can run in stealth mode
<u>Disadvantages</u>
- Can be affected by encryption
- Can be affected by switched networks
- The need for performance could lead to the detection of fewer attacks
- May fail to analyse attacks on a bust network

<h3>Detection methods</h3>
<b><i><u>Misuse detection</b></i></u>
Based on the comparison of system activity to a predefined pattern of events that describes a known attack
<b><i><u>Anomlay detection</b></i></u>
Based on the assumption that misuse or intrusive behaviour deviates from historical norms
<b><i><u>Specification-based detection</b></i></u>
Based on rules that define the correct operation of a program/ protocol
<b><i><u>Hybrid detection</b></i></u>
Combines detection models

<b>Response mechanisms</b>
<u>Passive</u>
Aims to notify other parties about the occurrence of an incident, and then rely on them to take further action. Alert admin/ SSO via email, pop-up windows, pager, SMS, or report to central network management console via SNMP traps. Most IDSs support these options.
<u>Active</u>
Aim to counter the incident that has occurred.
<h3>Detection imporvement</h3>
<b>Can detection be evaded?</b>
How can one fool a network IDS and avoid its detection?
<b><i><u>Insertion</b></i></u> 
IDS accepts a packet that the destination rejects
<b><i><u>Evasion</b></i></u>
Destination host accepts a packet that the IDS rejects
<b><i><u>Denial of Service</b></i></u>
The IDS is overwhelmed with traffic and is unable to analyse new packets

<b>String obfuscation</b>
A technique used to hide the content of a string within software code to prevent unauthorised access, reverse engineering or detection by security tools.
Example;
<font color="red">Write in lecture</font>

<h3>Intrusion prevention systems</h3>
<b>Automated responses</b>
Automated response is increasingly important in order to cope with modern IT/ OT/ IoT environments. Large systems can receive a large number of attacks. Implementing automated response solutions is far from perfect

<b>Countering intrusions</b>
- Intrusion detection systems (IDS)
	- Monitor networks, looking for indications of malicious activity
	- Have mainly passive responses
- Intrusion prevention system (IPS)
	- Positioned inline
	- Can respond in real-time
	- Proactively block detected attacks

<b>Terminating a session</b>
An IDS can terminate a session by sending a TCP RESET or ICMP unreachable error messages to one or both ends of a session. An IPS can lock the attack before it reaches its destination.

<h3>Prevention systems (NIPS)</h3>
<b><i><u>Content-based IPS</b></i></u>
- Cane be thought of as the intersection of firewall with IDS capabilities
- Like firewalls, it uses at least 2 network interfaces (internal, external)
	- Packets appearing at either interface are passed to the detection engine
	- Malicious packets and subsequent traffic are discarded
	- Acceptable packets are forwarded to the second interface
<b><i><u>Rate-based IPS</b></i></u>
- Also known as attack mitigators
- Monitor traffic flows instead of packet content
- Look for anomalies that could indicate Denial of Service attacks (DoS, DDoS) or scan attempts
<u>Advantages</u>
- Can prevent attacks before they reach their destination
- Easier to manage that HIPS
<u>Disadvantages</u>
- Requires careful planning, as it can have significant impact on existing network infrastructure
- Can be targeted as part of an attack
<b><i><u>Prevention systems (HIPS)</b></i></u>
- Operate above the OS kernel and services
- Intercept all requests to the system
- Monitor all system-API calls and block the ones that would result in malicious behaviour
- Usually incorporate application-level protection by inspecting data streams and the environment specific to an application (e.g., web server)
<u>Advantages</u>
- Usually performs misuse and anomaly detection
<u>Disadvantages</u>
- Future OS upgrades could cause problems
- Since it intercepts all system requests, it could inflict significant performance degradation on the system
<b>Intrusion prevention pros/ cons</b>
<u>Advantages</u>
- Can respond in real-time
<u>Disadvantages</u>
- Can introduce overhead
- Can represent single point of failure
- Can deny legitimate access in false alarm scenarios
- Needs to apply new signatures without sensor reboot

<b>Addressing IPS challenges</b>
- Single-point of failure
	- Use a back-up IPS (fail-over)
		- Expensive
	- Redirect traffic around the IPS
		- Provides no protection against attacks
	- Pre-configure IPS to run with minimum capabilities allowing all traffic to pass (fail-open)
		- Provides no protection against attacks
- False alarms
	- Respond only to alarms with high certainty
		- Can be applicable to only small set of alarms
		- Signature quality is a paramount at reducing false alarms







