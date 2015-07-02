##Website, Software and System Security## {#chapter9}

###Best Practices###

####9.1 Website Security####
This section has been heavily borrowed from the FLOSS manual on ‘Bypassing Internet Censorship-Best Practices for Webmasters’[^website_security]

##### 9.1.i Protect Your Website #####

- **Secure Hosting:** consider a secure website hosting option for your website (Refer to Tools & Templates section below for list of secure hosting providers). You may consider hosting your website in a foreign country, where the content is less controversial and legally protected. This may imply only a small additional delay in page load time (usually a few milliseconds) for your visitors and may save you a lot of trouble if you are located in a country where you web site's content is considered very controversial. You may also want to create a mirror server running as a standby to which you can switch easily.
- Protect your website against **DDoS attacks** by deploying open-source tools such as [Deflect](https://www.deflect.ca) by Equalit.ie. Deflect is a distributed infrastructure built to mitigate DDoS attacks and keep your website accessible at all times. While most secure hosting providers offer DDoS protection, its best to confirm. (Refer to Tools & Templates section below for other ways to protect against DDoS attacks). Its recommended to change the origin IP of the server (IP masking) for maximum DDoS protection- this new IP should not be publicaly advertised in DNS records. [^ipmasking]
- **Domain names:** Transfer your domain name and name servers to a secure DNS hosting provider or at least to a differnet provider that your normal webhosting . In case of attack against the web content , you will be able to easily point your domain name to a new hosting provider. In addition, when registering a domain name (for example: www.yoursitename.org), it may be good practice to register all accompanying TLDs such as .com, .net, .info or country-level-TLDs to protect your organization’s reputation against fake sites (such as www.yoursitename.com/ www.yoursitename.net) that a visitor may mistakely access instead of the main domain name: www.yoursitename.org.
- **Monitor logs:** Monitor website visitor logs and database user logs to track activity on the site to ensure they are valid connections and to identify anomalies.  (Refer to Chapter 7 - Monitor, Measure, Record). Monitoring traffic logs will enable you to learn something about the countries your visitors come from. If you notice a major drop in traffic from a specific country, your Web site may have been blocked.
- Protect your site from **SPAM** by enabling CAPTCHA on all site visitor submission venues.
- **Test and optimize** your website with the main circumvention tools your visitors are likely to use. Check and fix any broken pages or features. Ideally, make your website usable to visitors without JavaScript or plugins, since these may be unavailable or broken when people are using proxies.
- **User Roles & Permissions:** If your site is running on a content management system (CMS) such as Drupal or Wordpress, setup a roles-based-access policy for filtered permissions based on the user’s role -create separate roles for a site administrator versus a content manager, a site moderator and assign permissions based on the actions (principle of least privilege) that they are required to perform on the site. Protect the admin console by limiting it to authorized users only. Enforce a strong password policy on all user accounts (Refer to Chapter 2 for Password Policy recommendations); passwords should always be stored as encrypted values. Alternatively, you may choose to use a static website if the content does not need to be dynamic.
- **Site backups:** Ensure your site (code and database) are both backed-up frequently and are included in your disaster recovery plan (Refer to Chapter 8- Data Security, Backup & Recovery)
- **Data segmentation:** When using a content managment system (such as Drupal or Wordpress), limit connections to the database from just the webserver in order to minimize the risk of your data being exposed. If the database is running on a seperate server, ensure that the connection between the database and the webserver is encrypted (SSL-enabled) [^SSL]
- **Firewall & Ports:** Ensure you have a firewall setup, and are blocking all non-essential ports. (Refer to Chapter 7- Network Security); only allowing access to port 80 and 443 from the outside world.
- **Use alternative ports** to access site back-end. Hackers usually run automatic scans on standard ports to detect vulnerabilities. Consider changing your ports to non-standard values (such as SSH) to minimize the risks of these attacks.
- **Avoid using FTP** to upload your files. FTP sends your password over the Internet unencrypted, making it easy for eavesdroppers to steal your login credentials. Consider using FTPS (FTP with TLS) instead.
- **Be smart about the site error messages:** Be careful with how much information you give away in your error messages. For example if you have a login form on your website you should think about the language you use to communicate failure when attempting logins. You should use generic messages like “Incorrect username or password” so as to not give away the identity of the field that may be correct. If an attacker tries a brute force attack to get a username and password and the error message gives away when one of the fields are correct then the attacker knows he has one of the fields and can concentrate on the other field.
- **Audit your code:** Conduct an independent security audit to identify potential security holes before your site goes live.
- **Software updates:** Secure your Web site, especially if you use a CMS (Content Management System). Always install the latest stable updates to fix security flaws. Subscribe to the CMS' mailing list or follow security experts (via twitter or otherwise) to stay informed about new security vulnerabilities.
- **Test upgrades & patches** on a sandbox before pushing changes to the production server: while software upgrades and security patches are essential to keep your site protected, be sure to test them on a sandbox to ensure site functionality remains intact before pushing changes to the production server.

##### 9.1.ii Protect Your Visitors #####

Apart from protecting your Web site and yourself, it is also important to protect the visitors from potential third party monitoring, especially if they submit content to your website.

- **Enable SSL** on all your organization’s websites - facilitate best practices & security standards by installing a digital certificate on your website to ensure that visitors are connecting to your sites via an encrypted connection. Deploying HTTPS throughout your site makes it more difficult for eavesdroppers to look at the content which is being transferred and assures your identify to your site visitor. [SSLLabs](https://www.ssllabs.com/index.html) is a good resource to evaluate your site's SSL setup. 
- **Minimize retained data in your logs**. Avoid saving IP addresses or any personal data related to your visitors longer than necessary. Ensure that logs cannot be accessed with the same credentials (username/password) that are used to administer the website. 
- **Create a light and secure version** of your Web site, without any Flash or Javascript embedded code, compliant with Tor and low-bandwidth connections.
- **Site Privacy Policy:** If you site is collecting user information via a contact form or another mechanism, ensure your site’s privacy policy clearly states how collected information will be protected, in addition to not being shared with a 3rd party.
- **Educate your visitors:** Teach your users how to use circumvention tools, and be able to improve their online security by linking them to resource such as [SpeakSafe](https://speaksafe.internews.org) or [Security-in-a-Box](https://securityinabox.org). Make a digital safety checklist available so your visitors can be sure they are not being monitored or attacked.

##### 9.1.iii Protect Yourself #####

Here are some tips to prevent potential personal harm, if staying anonymous as a webmaster is important for you.

- **Go anonymous:** Use an anonymous email address and name which is never associated with your real identity.
- Use a service like **[Tor](https://www.torproject.org) to stay anonymous** when updating your Web site. Refer to Chapter 6 (Anonymity during Surfing) for more information on using Tor.
- Protect the identity of the domain name owner via **private domain registration**- even though this may be slightly expensive it can help protect your identity, and of your organization associated with a website - this is especially true if there are chances your site will be controversial in your country. Kindly note that if your domain registrar is based in your country, they would know the true identity of the domain owner based on information shared during the domain registration process. In most countries, domain registrars are ISPs who are state-regulated and if your site conveys an anti-government message, your domain registrar could be pressurized to share domain owner information with your adversaries. In this case, consider using a domain registrar in a foreign country.

##### 9.1.iv Preventing Website Censorship via Multiple Channels of Distribution #####

Webmasters can and should take different actions in order to spread their content as much as possible, to prevent being shut down or blocked.

-   Create **a mirror of your site** as a standby to which you can easily switch.
-   **Offer an API** (application programming interface), which allows others to access your content automatically via third-party software such as Twitter.
-   Set up a **RSS feed** and make sure it contains full articles and not only excerpts (snippets). This way your content can be parsed very easily by third party websites and applications, which can be used to read your content where direct access is blocked.
-   **Share your content** on popular social networking platforms, such as Facebook or Twitter, which may be hard to block.
-   **Spread the content** as much as possible. Make your content available for download. Wikipedia, for example distributes its entire content freely as a database dump that can used to easily create new mirror websites with the same content elsewhere.
-   Consider **publishing web articles under an open license** (like Creative Commons) that allows everyone to reuse your content and create mirrors. 

####9.2 Software Development Security####

- **Design Software with Secure Features**: Write code that incorporates security principles by design. Understand the security requirements for your visitors based on their scenario (audience location, website content, site engagement, your organization’s mission, risk to visitors) to help define a methodology that will cater to these unique security requirements. Using threat models to help identify security threats during the software design phase, before code is developed.
- Ensure **security is a consideration through the SDLC** (Software Development Lifecycle) from design, to development, user testing and rollout.
- Perform security **code reviews and security testing** (vulnerability and penetration) before deploying new software.
- Apply **security patches and software updates** to the test environment as well.

####9.3 System (Server) Security####

- Create a **network diagram** to understand your server architecture.
- **Patching and Keeping Software Updated**: Security patches (also, known as “service packs”) from the system vendors are released to close known security holes. Ensure that your systems (whether server OS, a content-management-systems or custom application) are up-to-date with the necessary security patches. Whenever a new service pack is available, you should carefully study the details of vulnerability it addresses and its impact on your systems. Depending upon the risk it addresses you may decide to apply it immediately or schedule a planned downtime (for example: a security update for your Drupal website could require the website inaccessible for some time). Create a communication plan to ensure that everyone affected by this downtime (for internal systems, this would include staff; for external systems such an organizational website, this would include donors, partners & the general public) are informed about the planned downtime. After applying the latest security patches, you should stay updated for new release of any software patches or firmware updates to hardware. Subscribe to software & vendor’s bulletins and ensure you have a support contract in place  (Refer to Chapter 5- Service Level Agreement for recommendations). 
- **Vulnerability Scans for your systems[^vulnerability]**: As a System Administrator, if you are aware of the vulnerabilities, you can take corrective action, before someone exploiting them. There are many security vulnerabilities that are specific to operating systems and there are tools available which scan the system to report security problems. Periodically scan your systems and after getting the report, you can analyze each vulnerability to understand it's impact in your system environment. If it security risk is serious, take corrective action immediately. Otherwise, plan for an earliest time slot, if the corrective action requires scheduled downtime of the system. Also, be sure to scan the system after fixing the vulnerability to make sure it has been fixed, and not mistakenly exposed other vulnerabilities .
- **Monitor your systems daily**: Just as you monitor your network traffic, its imperative to monitor your system & application logs as well. Check health of servers daily, such as storage space, LEDs on the server, network activity, user logins. Ensure you have a good log analyzer in place that can read these log reports, analyze trends on your system, create a summary report or statistics either in graphic or tabular form and send alerts for pre-defined threshold crossing alarms, login attempts and failures. (Refer to Chapter 7 for more best practices)
- **Antivirus & Anti-Malware software on servers**: Ensure servers are protected from malware and viruses.
- Remove unnecessary programs or services[^backup]: Uninstall any software and turn-off services not needed. Don't install desktop software such as email clients, chat programs on servers - these pose an unwarranted and needless risk. Keep software running on servers as simple as possible without sacrificing carefully evaluated functionality.
- **System access for contractors or vendors**: Ensure protocols are in place to screen contractors (external software developers) or vendors access to servers. Contractors and vendors need to abide by security policies and connect to systems via secure methods (SSH).
- Periodical **evaluate and test system security policies** to identify gaps.
- Obtain **public domain software (open source) from reputable sources**, and then check the newly downloaded software thoroughly, using reputable virus detection software on a locked disk, for signs of infection before copying it to a hard disk.[^software] Before you choose to download any software, make sure you are not violating copyright or other applicable laws.
- Leaving default and sample files located in **default directories** [^traffic] gives an attacker a potential edge by decreasing the amount of reconnaissance needed to inspect an environment. It also decreases the probability that the intrusion will be noticed.
- The **mail server**[^mail_server] is one of the easiest routes for virus attack through e-mail attachments. Mail server should be configured to block or remove email that contains attachments that are commonly used to spread viruses, such as .vbs, .bat, .exe, .pif, and .scr files.
- To **prevent spamming**, emails only authenticated by users in the organizations should be allowed.
- **Business Continuity Planning**: Ensure procedures are in place to ensure your systems, website and applications are backed-up, can be easily restored to ensure uninterrupted business continuity in the event of an interruption (software/hardware failure) or a catastrophe (theft, flood, fire, riots or an office raid). Refer to Chapter 8- Data Security, Backup & Restore.

####9.4 Security on End-User Devices####

- Install **licensed software** on end-users computers and ensure the necessary OS software patches are applied as well. You may be able to rely on getting discounted software licenses from an organization like TechSoup.
- Install **anti-virus and malware protection** on all devices. Auto-update for virus definitions should be enabled and their devices should be set to scan daily for viruses. For devices connected to the network, you may choose to push virus definitions via a central anti-virus server during low bandwidth usage periods such as after working hours or on the weekends.
- Practice the **principle of least privilege[^leastprivilege]:** this principle helps reduce the "attack surface" of the computer by eliminating unnecessary privileges that can result in network exploits and computer compromises. Ensure that staff do not have admin permissions when logging into their computers to accidentally install unauthorized software.
- Make **provisions for the use of removable media:** Removable media such as USBs, DVDs can contain viruses. Ensure that you set up a protocol to scan these devices on an external computer that is not connected to the office network before users plug them into their devices.
- Ensure that data on end-users desktops or laptops is **backed up regularly** to prevent catastrophic data loss in case of theft or hardware failure. (Refer to Chapter 8 on Data Security, Backup & Restore)
- Remove **unnecessary software and disable unnecessary services** (such as remote access) from computers.
- Enforce the **password policy** for their devices and online accounts; enable two-factor authentication for their email. (Refer to Chapter 2 on Password Policy)
- Ensure **physical security** of their devices (Refer to Chapter 10 on Physical Security).

####9.5 Secure Organizational Social Media Accounts####

Its easy to overlook social applications such as your organization’s Facebook page, twitter account or YouTube channel when you are focused on network security or protecting your sites against DDoS attacks. But these systems are equally susceptible to attacks and could, in fact, be the first entry point in tarnishing your organization’s reputation.

- As part of your organization’s Risk Assessment (Refer to Chapter 1), determine who has access to your organization’s social accounts - **limit access** to key stakeholders.
- Ensure these accounts follow the **password policy** standard (Refer to Password Policy in Chapter 2) - set a password age limit and update account passwords at regular intervals (every 3 months, at the very minimum).
- Review **security and privacy settings** for all accounts.
- Setup policies for **password recovery** to an organizational email address, instead of an individual email account - this would ensure no one person has access to these key institutional social assets.

###Tools & Templates###

- DDoS protection:
    -   [Deflect by Equalit.ie](https://www.deflect.ca)
    -   [Project Shield by Google](https://projectshield.withgoogle.com/public)
    -   [Project Galileo by Cloudflare](https://www.cloudflare.com/galileo)
- Secure Hosting:
    -   [Greenhost.nl](https://greenhost.net)
    -   [Team Cymru](http://www.team-cymru.org)
    -   [VirtualRoad/Qurium](https://www.qurium.org/services/)
    -   [EEF’s Guide on chossing a web host](https://www.eff.org/keeping-your-site-alive/choosing-a-web-host)
- SSL Evaluator:
-   Test your site's SSL setup: [SSLLabs](https://www.ssllabs.com/index.html) 
- [Secunia Personal Software Inspector (PSI) available for Windows OS]((http://secunia.com/vulnerability_scanning/personal))

###Recommended Reading###

- [Secure hosting guide](https://equalit.ie/)
- [eQualit.ie recommended list of hosting providers](http://wiki.deflect.ca/wiki/ISP_reviews)
- [EFF, Choosing a Web Host](https://www.eff.org/keeping-your-site-alive/choosing-a-web-host)
- [Huridocs, 10 tips to keep your website safe](https://www.huridocs.org/2013/08/10-tips-to-keep-your-website-safe)
- [Internews, My Website Is Down](:https://github.com/OpenInternet/MyWebsiteIsDown/blob/master/MyWebsiteIsDown.md)
- [National Network to End Domestic Violence, Technology & Confidentiality Resources Toolkit](http://tools.nnedv.org/tipsheets-charts)

###Chapter References###

- [SANS Institute, System Administrator-Security Best Practices](http://www.sans.org/reading-room/whitepapers/bestprac/system-administrator-security-practices-657)
- [Indiana University, Best practices for computer security](https://kb.iu.edu/d/akln)
- [Microsoft, Data Security and Data Availability in the Administrative Authority](https://msdn.microsoft.com/en-us/library/cc722918.aspx)
- [DarkReading, The Five Most Common Security Pitfalls In Software Development](http://www.darkreading.com/the-five-most-common-security-pitfalls-in-software-development/d/d-id/1140103?)
- [Safecode.org, Fundamental Practices for Secure Software Development](http://www.safecode.org/publication/SAFECode_Dev_Practices0211.pdf)
- [Mano Paul, CSSLP, CISSP, AMBCI, MCAD, MCSD, Network+, ECSA, The Ten Best Practices for Secure Software Development](https://www.isc2.org/uploadedfiles/(isc)2_public_content/certification_programs/csslp/isc2_wpiv.pdf)
- [Developer.com, 10 Best Practices for Secure Software Development](http://www.developer.com/white_papers/article.php/384488/10-Best-Practices-for-Secure-Software-Development.htm)
- [BuildItSecure.ly](http://builditsecure.ly/)
- [NetworkWorld, Anti-virus best practices](http://www.networkworld.com/article/2330116/lan-wan/anti-virus-best-practices.html)
- [NetApp, Antivirus Scanning Best Practices Guide](http://www.netapp.com/us/system/pdf-reader.aspx?m=tr-3107.pdf&cc=us)
- [TechRadar, Best antivirus: 10 home security suites reviewed and rated](http://www.techradar.com/us/news/software/applications/best-antivirus-10-programs-on-test-924608)
- [PCMag, The Best Antivirus for 2015](http://www.pcmag.com/article2/0,2817,2372364,00.asp)
- [BeyondSecurity, Web Security Basics](http://www.beyondsecurity.com/web-security-and-web-scanning.html)
- [CreativeBloq, 10 security tips to protect your website from hackers](http://www.creativebloq.com/web-design/website-security-tips-protect-your-site-7122853)
- [National Network to End Domestic Violence, Technology Safety Organizational Technology Capacity & Development (for Agencies & Programs Working With Survivors)](http://nnedv.org/resources/safetynetdocs/154-organizational-technology-capacity-development.html)
- [NIST, Security Considerations in the System Development Life Cycle](http://csrc.nist.gov/publications/nistpubs/800-64-Rev2/SP800-64-Revision2.pdf)
- [NIST, Guidelines on Security and Privacy in Public Cloud Computing](http://csrc.nist.gov/publications/nistpubs/800-144/SP800-144.pdf)
