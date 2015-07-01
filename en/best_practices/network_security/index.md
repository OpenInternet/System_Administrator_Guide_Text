##Network Security## {#chapter7}

####Best Practices####

##### 7.1 Monitor, Measure, and Record #####

This is the golden rule for all sysadmins - understand the traffic on your network. Get/build/buy a system to monitor, measure, record and analyze network traffic. It may be prudent to regularly share network analysis reports with key stakeholders and staff to help them understand the various threats to the network. In addition to raising their awareness on the network security challenges faced by the organization, it also would allow for enhanced investment in security technology and digital security education & training for staff (Refer to Chapter 4- Budgeting for Tech)

Here is a recommended shortlist of things [^monitor] to start monitoring/recording/charting/graphing:
- Load average
- Memory usage
- Disk I/O (transactions per second)
- Network throughput (in Mbits/sec)
- Network throughput per virtual host/site
- Transfer (in GB/month)
- Transfer per virtual host
- Disk storage (monthly in GB) and also daily rolling average if files are uploaded and deleted regularly
- Average response time of a PHP (or Ruby/Python/etc.) page under your control that does not change. Testing real web pages gives you a consistent baseline that you can use to narrow the problem to the server, the OS, or the web code itself.
- SSH logins per day/month by user and IP address

Once you have consistent information, you’ll start seeing patterns and can look for things out of the ordinary/abnormal traffic. It’s also good for correlating data to behaviors when you’re troubleshooting issues and aren’t sure where to start.

##### 7. 2 Effective Firewall Management #####

Following these best practices [^firewall_management] and conducting regular maintenance work can make the life of a system administrator less stressful and help better protect your network.

- Conduct daily maintenance tasks: As stated above under “Monitor, Measure & Record”, review traffic logs & check for any alerts.
- Deny all traffic by default and only open specific ports, protocols and services as needed.
- Change the default administrator or root password on the firewall to a complex, long passphrase. Set a reminder to change the firewall admin password every 6 months.
- Monitor the CPU usage & network throughput of the firewall to ensure applications installed on it (such as an anti-virus, VPN software) are not slowing it down.

*Review firewall policies regularly* [^fw_policies]

- Over time, firewall policies become outdated. Servers that were published to the internet get decommissioned, and services get moved to new servers. But firewall policies tied to decommissioned servers often are not removed or updated. The danger here is that IP addresses of decommissioned servers get reused on new servers, and new servers can then easily be published for unintended services.
- Change Management protocol: Regular overview of the policies is even more important if there is more than one system administrator. In such environments, it is likely that, for example, two administrators created two different policies for same network traffic specifications. When conducting policy reviews, see if you can consolidate any of the policies. Establish a change management protocol to document all firewall changes when there is more than one system administrator.
- Review rules that clients use to connect to different services on the internet. An application that required a specific port to communicate with the internet might have been updated with a new application that uses a different port. Ensure that accurate ports only allow access to specific applications.
- Get a “trusted, independent” audit: When possible, allow someone who has knowledge of and experience with managing firewalls but who is not involved in the day-to-day operations of your network to audit the firewall policies - this would ensure a trusted, fresh perspective and will help identify any policy conflicts.
- It’s recommended to review the firewall policies at least twice a year.

*Back up your firewall regularly* [^firewall_management]

- Make a backup of firewall policies and configurations before performing any policy changes. With a backup, if you run into any problems with new policy configuration, it is easy to revert back to the previous, working configuration.
- Consider what else is needed to restore your firewall if disaster recovery is necessary. Are there any specific routes that are not included in the firewall configuration backup, but are required for complete restore? How about certificates and their corresponding private keys that might be used for SSL session termination on the firewall?
- Practice firewall recovery in test environment. Testing should point out any missing components in the backup and, therefore, give administrators the opportunity to learn the necessary skills to perform a quick and reliable restore when necessary.

*Update the firewall* [^firewall_management]

- Regardless of the make and model of your firewall, you should regularly update your firewalls. All firewall manufacturers release updates for their products. These updates often include bug fixes and new features that can help mitigate new types of threats, thereby minimizing risk.
- When possible, also update network card drivers. These updates often solve problematic behaviors, including those that might, at first, seem to be related to an unreliable firewall.

##### 7.3 Intrusion Detection and Prevention System (IDPS) #####

Today’s malware is so advanced that a firewall alone will leave a network vulnerable. A firewall provides a basic line of defense (analyzes packet headers and enforces policy based on protocol type, source address, destination address, source port, and/or destination port) by allowing or blocking connectivity to the network through port connections. You may think of a firewall like a house - it allows you to close and lock the doors and windows you don’t want outsiders to have access to, while keeping them open for welcome visitors.

The problem with this defense is that the firewall does not investigate the data that is allowed to enter the doors on the network. If there is danger lurking outside the front door (port connection) and the data finds a way into the home (the network), it will cause an intense amount of damage. And, although it’s not practical to check your guests’ bags, it is necessary to scan all items entering your network to determine if they are friend or foe because the network’s health and safety rely on it. An IDPS is the answer to address this challenge.

An Intrusion Detection and Protection System (IDPS) is the newest line of defense in network security and combines two levels of network protection into one. Intrusion detection accomplishes traffic analysis in order to detect malware & produces reports while Prevention actively blocks the malware on the network by dropping the malicious data while still allowing normal data to continue on the network. This system identifies and prevents malware intrusion by examining information (whole packets, both header and payload, against a library of known attacks) via sensors within the network infrastructure.[^idps]

For added protection, you may adopt the “anomaly detection” versus a “misuse detection” approach via an IDPS. In misuse detection, the IDS analyzes the information it gathers and compares it to large databases of attack signatures. That is, the IDS looks for a specific attack that has already been documented. Much like a virus detection system, detection software is only as good as the database of intrusion signatures that it uses to compare packets against. However, in anomaly detection, the system administrator has more control and can define the baseline, or normal, state of the network's traffic load, breakdown, protocol, and typical packet size. The anomaly detector monitors network segments to compare their state to the normal baseline, looks for anomalies and alerts the system administrator when one is detected.

In order to set up proper network security, layers of software, and solutions need to be in place that protect against various threats. Firewalls, anti-virus programs, access controls, and an IDPS solution (such as Snort) are all necessary to achieve effective network security.

##### 7. 4 Access Control & Authorization #####

Access is the ability to perform a function with a computer resource (e.g., use, change, or view).  Access controls are the system-based means by which the ability is explicitly enabled or restricted in some way.  Access controls can prescribe not only who (a user) or what (a process) is to have access to a specific system resource, but also the level of access that is permitted. [^access_auth]

Authentication is the means of establishing the validity of this claim.  There are three means of authenticating a user’s identity which can be used alone or in combination: something the individual knows (a secret –e.g., a password, Personal Identification Number (PIN), or cryptographic key); something the individual possesses (a token – e.g., a bank’s ATM card or a smart card); and something the individual is (a biometric – e.g., characteristics such as a voice pattern, handwriting dynamics, or a fingerprint). [^access_auth]

In most cases, we rely on passwords (something the individual knows) to authenticate end-users to our systems.

Based on your organization’s risk assessment (Refer to Chapter 1) and working with your organization’s stakeholders, create a process to authorize and document access privileges based on a legitimate and demonstrated need to have system access. Creating access modes or levels will allow you to isolate threats to limited areas on the network and will allow for focused problem-solving in case of an attack.
Access control to IT systems and data repositories should be based on the following access criteria, as appropriate:

- Identity (user ID): The identity must be unique in order to support individual accountability.
- Roles: Access to information must also be controlled by the job assignment or function (i.e., the role) of the user who is seeking access.
- Access Modes: Consider the types of access, or access modes - common access modes, which can be used in both operating and application systems, include read, write, execute, and delete.
- Location: Where appropriate, access to particular system resources (especially, to sensitive data repositories) will be based upon physical or logical location.

Ensure the following best practices with regards to authentication:
- Require Users to Authenticate: users must authenticate their claimed identities on all IT resources and data repositories. During the first instance of access with a new account, the initial password must be changed by the individual responsible for the account, in compliance with the defined password policy. Enable 2-factor Authentication. (Refer to Chapter 2 on Password Policy)
- Limit Log-on Attempts: The organization facilities must limit the number of log-on attempts to five (5).  This helps to prevent guessing of authentication data.  Where round-the-clock system administration service is available, system administrator intervention will be required to clear a locked account.  Where round-the-clock system administration service is not available, accounts will remain locked out for at least ten (10) minutes.
- User Account Review: When system users are no longer part of an organization, or their duties change, their account access must be appropriately modified or terminated.  Requests to change access privileges must be signed and forwarded to the appropriate designated individual by the responsible manager. Create a process to regularly review and audit user account access to IT systems & data repositories- this initiative may closely tie in with your organization’s employee onboarding and termination process to take the necessary action of account creation, modification or deletion.
- Use of the default “Guest” accounts is strongly discouraged on servers and workstations but, if needed, these accounts must conform to the naming conventions and the password policy established in this policy. Additional measures, such as disabling, renaming, or decoying these standard accounts, should be employed.
- Administer Data Properly: Establish procedures to disable lost or stolen passwords and monitor systems to look for stolen or shared accounts.

##### 7.5 Network Zones & Data Segregation based on Sensitivity #####

A common practice of protecting sensitive data against threats is setting zones of segregation based on access - this could be as simple as setting up a separate WAPs (wireless access points) for organizational staff and another for guests to connect to.

Taking this practice a step further, classify your data based on sensitivity (Level 1- Public, Level 2- Internal, Level 3- Confidential such as financial records, employee data, donor reports) during your organization’s risk assessment (Refer to Chapter 1) and set up separate network partitions that allow only authorized staff to access this data. Using this method would ensure that if an information breach occurs in one area, the other areas of data are protected from exposure.

Classification of your data based on sensitivity would allow you to create the appropriate security policies for access (access control), storage (network partitions, backups) and communication (encrypted channels) of this data.

##### 7.6 Alerts to recognize Abnormal Traffic Behavior #####

You may setup simple scripts to send you alerts to monitor the following recommended abnormal traffic behavior. However, remember that doing so may generate denser and larger logs that may be difficult to analyze.

- Port scans - opening of ports in an attempt to enumerate services.
- Attempted DNS zone transfers.
- E-mail reconnaissance - repeated failed attempts to variations of a user's name may give away information about infrastructure.
- Ping sweeping - pinging multiple hosts on a network in succession in an attempt to enumerate information about infrastructure and placement of devices.
- Web snaking - multiple ‘Get’ commands that download the entire contents of a website and attempt to enumerate subdirectories or download scripts.
- CPU Usage and memory leaks on servers
- Unauthorized modification of system and configuration files

##### 7.7 Advanced Traffic Filtering #####

- Multi-layer firewall: Networks can be threatened in a variety of ways. Maximize network security with packet, circuit, and application-level traffic screening to reduce the risk of unauthorized access.
- Smart application filters: Control application-specific traffic, such as electronic mail and streaming media, with data-aware filters to enhance security. Smart Application Filters recognize content and apply policy as the content traverses the network.
- Dynamic IP filtering: Reduce the risk of external attacks by restricting access to an as-needed basis and opening ports only for active sessions.

##### 7.8 System Audit Logs #####

An audit trail (also called audit log) is a security-relevant chronological record, set of records, and/or destination and source of records that provide documentary evidence of the sequence of activities that have affected at any time a specific operation, procedure, or event. In information or communications security, information audit means a chronological record of system activities to enable the reconstruction and examination of the sequence of events and/or changes in an event (For example: understanding a virus attack on the network or unauthorized access to confidential data).

Some applications generate their own log files, while others use the logging capabilities of the OS on which they are installed. Applications vary significantly in the types of information that they log. The following lists some of the most commonly logged types of information and the potential benefits of each [^log_management]:

- Client requests and server responses, which can be very helpful in reconstructing sequences of events and determining their apparent outcome. If the application logs successful user authentications, it is usually possible to determine which user made each request. Some applications can perform highly detailed logging, such as e-mail servers recording the sender, recipients, subject name, and attachment names for each e-mail; Web servers recording each URL requested and the type of response provided by the server; and business applications recording which financial records were accessed by each user. This information can be used to identify or investigate incidents and to monitor application usage for compliance and auditing purposes.
- Account information such as successful and failed authentication attempts, account changes (e.g., account creation and deletion, account privilege assignment), and use of privileges. In addition to identifying security events such as brute force password guessing and escalation of privileges, it can be used to identify who has used the application and when each person has used it.
- Usage information such as the number of transactions occurring in a certain period (e.g., minute, hour) and the size of transactions (e.g., e-mail message size, file transfer size). This can be useful for certain types of security monitoring (e.g., a ten-fold increase in e-mail activity might indicate a new e-mail–borne malware threat; an unusually large outbound e-mail message might indicate inappropriate release of information).
- Significant operational actions such as application startup and shutdown, application failures, and major application configuration changes. This can be used to identify security compromises and operational failures.

A log management infrastructure consists of the hardware, software, networks, and media used to generate, transmit, store, analyze, and dispose of log data. Some major factors to consider in the design of a log management system include:

- Volume of log data to be processed- many logs have a maximum size, such as storing the 10,000 most recent events, or keeping 100 megabytes of log data. When the size limit is reached, the log might overwrite old data with new data or stop logging altogether, both of which would cause a loss of log data availability. To meet your organization’s data retention requirements in compliance with local laws, you might need to keep copies of log files for a longer period of time than the original log sources can support, which necessitates establishing log archival processes. Because of the volume of logs, it might be appropriate in some cases to reduce the logs by filtering out log entries that do not need to be archived.
- Network Bandwidth - ensure that all logs are generated during off-peak hours to allow the necessary bandwidth during work hours.
- Time and resources needed for staff to analyze the logs
- Define a log rotation and archival process
- Retention Policy - understand the local laws pertaining to retention of data for legal purposes (evidence generation) and for audits & compliance efforts, especially financial and tax data
- Monitoring the status of the log management infrastructure (e.g., failures in logging software or log archival media, failures of local systems to transfer their log data) and initiating appropriate responses when problems occur.
- Security considerations related to online and offline data storage of log data. The confidentiality and integrity of the archived logs (on removable media) need to be protected, similar to backup data tapes (Refer to Chapter 8- Data Retention). In addition, ensure that old log data is disposed of properly once it is no longer needed.
- Maintaining the security of the log management infrastructure, including testing and implementing upgrades & updates to the log management infrastructure components - software & hardware.
- Re-configure logging as needed based on policy changes, technology changes, and other factors.
- Monitor and document anomalies in log settings, configurations, and processes.

##### 7.9 Remote Access #####

These days, most applications allow web-access for staff working remotely (for example: a SSL-connection to the office exchange server via Outlook Web Access or via an email client), as such, its imperative to understand why remote access is required to your network and to which applications.

Based on your organizational Risk Assessment (Refer to Chapter 1), understand the risks associated of providing remote access to your network and weigh the benefits against these risks.

However, if staff do require access to their office computer or a specific application (example: a contact database, a financial system or a network drive) from a remote location, here are a few guidelines to ensure you are reducing the risk of compromise to your network:

- Require staff to use a VPN (Virtual Private Network) to connect to your network - this creates an encrypted tunnel from their internet access/ISP (internet service provider) to your network.
- Provide remote access to specific ports on your network.
- Change the listening port for incoming connections (SSH, RDP). Remember to update any firewall rules with the new port.
- Provide remote access to only specific applications on your network.
- Provide remote access via only specific devices (computer or mobile) and usernames to your network.
- Establish a protocol (usage policy) for off-site care of confidential data and the rules for use of home desktops or mobile devices (licensed software, antivirus, security patches on all computers accessing the network, personal firewall enabled, encrypted connection and strong passwords on user accounts)
- Monitor remote access via VPNs and create alerts to ensure you are aware of unauthorized access to systems or data.
- Enable two-factor authentication on all sensitive systems. Ensure a user-account lockout policy is in place to lock an account for a period of time after a number of incorrect password guesses, this will help prevent hackers from using automated password guessing tools from gaining access to your system. Refer to Chapter 2 on Password Policy to ensure strong authentication standards & protocols are in place.

##### 7.10 Secure WiFi #####

Wireless networks can provide an unintended open door to your business network. Recommended tips for securing a wireless network:

- Change the wireless network hardware (router /access point) administrative password from the factory default to a complex password (Refer to Chapter 2 for password best practices). Save the password in a secure, encrypted location as it will be needed to make future changes to the device. In addition, set an alert to change the password on your wifi router at regular intervals - once a month is an ideal time frame. Be sure to communicate the new password to all staff.
- Disable remote administration of the wireless network hardware (router/access point).
- If possible, disable broadcasting the network SSID.
- Enable encryption- A wireless network deployed without adequate encryption is similar to a house without a front door with a welcome mat saying thieves are welcomed here at any time. If your device offers WPA encryption, secure your wireless network by enabling WPA (WPA2 is stronger) encryption of the wireless network. If your device does not support WPA encryption, enable WEP encryption.
- If only known computers will access the wireless network, consider enabling MAC filtering on the network hardware. Every computer network card is assigned a unique MAC address. MAC filtering will only allow computers with permitted MAC addresses access to the wireless network.
- Avoid your wifi router from getting targeted from hackers or curious minds in the neighborhood, use a non-descript SSID (Service Set IDentifier) for your organization’s wifi connection. This would reduce visibility of the wifi connections to your organization, as such, creating a level of “anonymity”.
- Set up zones of segregation based on access - this could be as simple as setting up a separate WAPs (wireless access points) for organizational staff and another for guests to connect to. Discourage staff from sharing the staff wifi password with guests - help them understand the risks. Set a schedule to change the wifi passwords regularly.
- Check the access point manufacturer’s website regularly for firmware updates and apply accordingly.
- Encourage holistic security practices, and during trainings & staff awareness workshops (Refer to Chapter 3), discuss the importance of securing their home WAP (wireless access points) with staff.
- Encourage staff to use a VPN such as Psiphon when connecting to public, unsecured WAPs (such as wifi in a cafe or at the airport) for browsing the Internet or accessing work email.

##### 7.11 Mitigating “Insider” threats #####

Institute stringent access controls and monitoring policies on privileged users, including technical staff. System administrators and privileged users have greater access to systems, networks, or applications than other users, thus posing an increased risk. While working through your organization’s Risk Assessment (Refer to Chapter 1), ensure that you identify privileged users, including technical staff, who have greater access to your systems. Create the necessary policies and identify accountability practices in collaboration with key decision-makers to ensure your organization’s information will be protected against “insider” threats. Some of these approaches include:

- Separating duties and requiring actions by multiple users address the need for stringent access controls and monitoring policies on privileged users (including system administrators).
- A privileged user can be prevented from maliciously altering the system if he or she is not permitted or technically able to release changes to the production environment without action by at least one other user.
- Consider having privileged users sign a privileged user agreement or rules of behavior that outlines what is required of them.
- Finally, as part of the employee exit procedure (Chapter 2- Policies), be especially careful to disable system access to former system administrators and technical or privileged users.

##### 7.12 Develop a system for day-to-day work #####

Create a checklist of tasks that need to be performed on a daily basis - some of these may include: checking monitoring consoles for alerts, storage capacity of backup tapes & logs, reading blogs & websites for new security threats, vendor websites for firmware updates. Allocate time at the beginning of the day to complete your daily checklist of tasks before moving on to other tasks.

##### 7.13 Document Everything #####

As challenging as it is, you must document standard procedures, connectivity information, regular maintenance tasks, and disaster recovery contingency plans. Documentation is difficult because it requires the System Administrator to stop and move stepwise through each task, while thoughtfully documenting each procedure. It's time-consuming and labor-intensive to thoroughly document, take screenshots, describe procedures, and explain possible outcomes.

However, standard procedures help you maintain consistency and reproducibility in your computing environment. Creating and adhering to a set of standard procedures has the added effect of stabilizing your systems and services, which, in turn, stabilizes your company's overall productivity.
Moreover, detailed documentation of changes made (for example: when reacting to a security incident) will go a long way in helping you investigate future network failures or potential conflicts. As such, it is highly recommended that sysadmins create a simple protocol of documenting all changes to all systems on the network, such as the firewall, router, server, WAP (wireless access point) configuration.
Good documentation does pay-off in the end, especially during an emergency such as a hardware failure when you need to re-configure your server or during a network conflict when you are trying to trace down an anomaly. Ensure that these configuration notes are saved securely and accessible easily in case of emergencies.

##### 7.14 Develop project management habits #####

It may be beneficial to adopt simple project management practices even for small, one-person projects. Write up a small scope of work, write requirements, get sign-off from stakeholders on their expectations, plan a schedule, and record your activities. Write up a postmortem document at the end. Even if it’s just for yourself. It doesn’t have to be fancy, and it certainly doesn’t have to be formal PMBoK activities. It may seem bureaucratic managing all that paper and it may seem like you’re spending more time on paperwork than system administration, but it helps keep you organized, helps you prioritize competing tasks and communicate effectively with your supervisors.

##### 7.15 Keep yourself updated #####

Staying in tune with current best practices, industry trends and emerging threats will help you learn about possible attacks to your network. Its recommended for sysadmins to sign-up to security mailing lists, read security news sites, receive information guides & updates shared by vendors and follow security researchers via twitter to ensure that they are always “in-the-know” when it comes to security trends and threats. (Refer to "Community Resources" towards the end of this guide for websites and mailing lists followed by sysadmins in the Internet Freedom community).

###Tools & Templates###

- Intrusion Detection & Prevention System (IDPS): [Snort](https://www.snort.org)
- VPN: [Psiphon](https://psiphon.ca/); [RiseupVPN](https://help.riseup.net/en/vpn)

###Recommended Reading###

- [Engine Room Checklist](https://github.com/the-engine-room/responsible-data/tree/master/organizational-security-atomized-plan)
- [NIST, Guide to General Server Security](http://csrc.nist.gov/publications/nistpubs/800-123/SP800-123.pdf)
- [NIST, An Introduction to Computer Security](http://csrc.nist.gov/publications/nistpubs/800-12/handbook.pdf)
- [NIST, Guide to Intrusion Detection and Prevention Systems (IDPS)](http://csrc.nist.gov/publications/nistpubs/800-94/SP800-94.pdf)

###Chapter References###

- [SANS Institute, Essential Information Security For Corporate Employees](http://www.sans.org/reading-room/whitepapers/awareness/essential-information-security-corporate-employees-1179)
- [SANS Institute, System Administrator - Security Best Practices](http://www.sans.org/reading-room/whitepapers/bestprac/system-administrator-security-practices-657)
- [NIST, Guide to Computer Security Log Management](http://csrc.nist.gov/publications/nistpubs/800-92/SP800-92.pdf)
- [NIST, Audit Trails](http://csrc.nist.gov/publications/nistbul/itl97-03.txt)
- [Commonwealth of Pennsylvania, IT Audit Logging Standard](http://www.dpw.state.pa.us/cs/groups/webcontent/documents/communication/p_031981.pdf)
- [United States Patent & Trademark Office, Network Audit, Logging and Monitoring Policy](http://www.uspto.gov/about/vendor_info/current_acquisitions/sdi_ng/ocio_6011_09.pdf)
- [NIST, Guidelines on Firewalls and Firewall Policy](http://csrc.nist.gov/publications/nistpubs/800-41-Rev1/sp800-41-rev1.pdf)
- [NETSPI, Firewall configuration checklist](https://www.netspi.com/Portals/0/docs/Blog_Documents/EH_Firewalls/Firewall_Audit_Checklist_Short_v1.pdf)
- [Windstream, Is Your Network Safe Behind Just A Firewall](http://www.windstreambusiness.com/resources/whitepapers/is-your-network-safe-behind-just-a-firewall)
- [Cisco, Network Security Policy](Best Practices White Paper: http://www.cisco.com/c/en/us/support/docs/availability/high-availability/13601-secpol.html#t4)
- [National Network to End Domestic Violence Technology Safety Organizational Technology Capacity & Development (for Agencies & Programs Working With Survivors)](http://nnedv.org/resources/safetynetdocs/154-organizational-technology-capacity-development.html)
- [CERT, Common Sense Guide to Mitigating Insider Threats 2013:](https://www.cert.org/blogs/insider-threat/post.cfm?EntryID=139)
- [eSecurityPlanet, 5 Best Practices for Securing Remote Access](http://www.esecurityplanet.com/trends/article.php/11164_3937121_2/5-Best-Practices-for-Securing-Remote-Access.htm)
- [ITTechNewsDaily, 5 Best Practices for Managing Remote Access:](http://www.ittechnewsdaily.com/175-managing-remote-access-security.html)
- [Berkeley Security, Securing Remote Desktop for System Administrators](https://security.berkeley.edu/content/securing-remote-desktop-system-administrators)
- [Dr. Eric Cole, Secure Anchor 2006](http://www.securityhaven.com/docs/Security_Best_Practices.pdf)
- [Internap, April 2013- 5 best practices for successful system administration](http://www.internap.com/2013/04/10/5-best-practices-for-successful-system-administration/)
- [ZDNet, March 2013- 10 security best practice guidelines for businesses](http://www.zdnet.com/article/10-security-best-practice-guidelines-for-businesses/)
- [TechNet, April 2011- Simple Firewall Best Practices for Small and Midsize Businesses](https://technet.microsoft.com/en-us/security/hh144813.aspx)
- [Kevin Beaver, CISSP](http://www.principlelogic.com/docs/firewall_best_practices.pdf)
- [Vinod Mohan, SolarWinds Worldwide, LLC 2013](http://cdn.swcdn.net/creative/v9.3/pdf/Whitepapers/Best_Practices_for_Effective_Firewall_Management.pdf)
- [NIST, Guidelines for Securing Wireless Local Area Networks (WLANs)](http://csrc.nist.gov/publications/nistpubs/800-153/sp800-153.pdf)
- [Webopedia, Intrusion Detection (IDS) and Prevention (IPS) Systems](http://www.webopedia.com/DidYouKnow/Computer_Science/intrusion_detection_prevention.asp)
- [David Piscitello, Intrusion Detection… Or Prevention](http://www.corecom.com/external/bcrmag/bcrmag-ids-may02.pdf)
- [SANS Institute, Critical Security Controls](https://www.sans.org/critical-security-controls/controls)
- [SANS Institute, Monitoring Security and Performance on Converged Traffic Networks](http://www.sans.org/reading-room/whitepapers/analyst/monitoring-security-performance-converged-traffic-networks-34720)
- [NIST, Guidelines for the Selection, Configuration, and Use of Transport Layer Security (TLS) Implementations](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)
- [NIST, Guide for Security-Focused Configuration Management of Information Systems](http://csrc.nist.gov/publications/nistpubs/800-128/sp800-128.pdf)
