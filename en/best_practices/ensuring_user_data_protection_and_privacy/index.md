##Ensuring User Data Protection & Privacy## 
{#chapter6}

While access to sensitive data on the network is governed via “Access Control” (Refer to Chapter 7 on Network Security), you can assist with additional privacy to users by ensuring they adopt the following secure data communication and storage practices, provided these practices constitute approaches identified during the organization’s Risk Assessment (Refer to Chapter 1). Keep laws and regulations related to encryption in mind before recommending these best practices.

###6.1 Encrypt User Data-at-Rest###

Data-at-Rest refers to user information stored on their devices, in external hard drives and on removable media such as USBs, DVDs.

#### 6.1.i Full Disk Encryption (FDE) ####

When working with users at a media or a human rights organization, it’s imperative to safeguard their information on their devices. Having made the business case for encrypting data (Refer to Chapter 1 for Risk Assessment) and after taking into consideration laws governing your organization (Refer to Chapter 11- Know Your Rights), institute the policy to encrypt all hard-drives to plan against stolen or confiscated devices.

"Full disk encryption (FDE) enables strong encryption algorithms to automatically protect all data stored on the hard drive of user’s PCs and laptops. With FDE, data is encrypted automatically when it's stored on the hard disk. This is different from file or folder encryption systems, where it's up to the user to decide which data needs encrypting. FDE's biggest advantage is that there's no room for error if users don't abide by or don't understand encryption policies", as explained by Mary Brandel in his article [^FDE] published in ComputerWorld.

Here are some best practices when instituting Full Disk Encryption (FDE):

- Prep the machine: Before enabling encryption on the HDD, ensure the machine is clean and running properly beforehand. It’s essential that there are no disk problems that would render code specific to the encryption engine to be unreadable.
- Its recommended to defragment the hard drive, run checkdisk several times, back up the data, administer all patches and optimize performance before encrypting.
- Test the waters: Test encryption on a few “pilot” testers - these could be your tech champions to iron out the kinks, gauge user resistance and the scope of the full deployment, before instituting FDE across the organization. (Refer to Chapter 3 for change management best practices).
- Don’t underestimate deployment time; enabling FDE takes time, especially for large drives. A good rule of thumb is that it takes anywhere between 4-6 hours depending on the size of the HDD for the software to encrypt the drive.
- Check for interference with other applications. Another reason for a pilot test is to identify if there is device-driver or BIOS interference between the encryption software and other applications. Run tests for the various operating systems of devices on your network as not all of them may be compatible with your FDE solution.
- Ensure users are employing secure storage practices & strong creation policies for their pre-boot password.
- Key recovery: Help users understand the implications if they forget their pre-boot password. Ensure that they have a mechanism of regularly backing-up their data, in case their device needs to be re-formatted in order to start from scratch without the pre-boot password. (Special considerations needed to put in place when staff use personal devices for work purposes that do not automatically connect to the network backup system). You may consider implementing “key escrow” for encryption keys associated with work devices. However, careful mechanisms needs to be put in place to ensure that escrowed keys are kept super secure, and a policy is defined and clearly communicated with respect to key access request (for example: a supervisor cannot access their subordinate’s data without prior permission) and the responsibility of the technical person in charge of granting access.

##### 6.1.ii Encrypt Passwords #####

Institute a policy for the use of password managers (such as KeePass) to store passwords in irreversible encrypted form. As the name implies, password managers make password management effortless, especially as end-users adopt best practices such as using a different password for each account, while they also assure security, by protecting end-users against keyloggers (malware). Encrypted passwords are harder to crack further enhancing user data privacy. (Refer to Chapter 2 for further best practices on password management.)

##### 6.1.iii Encrypt Removable Media #####

With the prevalence of USB drives & external HDDs, more attention is being paid to removable media encryption and device control. Train users on encrypting the entire USB drive before storing data on it - this is especially critical when users are traveling with sensitive data while crossing borders and protection against data leaks in the event of device loss or theft. Ensure encryption of personal devices (laptops & phones) used to access organizational data is addressed under the BYOD policy. (Refer to Chapter 2 for best practices with respect to the BYOD policy.)

##### 6.1.iv Encrypt Backup Tapes #####

Employ secure data backup practices and ensure that data is encrypted on servers and in backup media (such as tapes). This would ensure added security in case of an office raid if servers & backup tapes are confiscated or in case of loss or theft of tapes. (Refer to Chapter 8- Data Security, Backup & Restore for additional best practices to protect data on servers.)

#### 6.2 Encrypt User Data-in-Transit ####

Data-in-Transit refers to user information shared via emails, instant messages/chats, text messages (SMS) and phone calls.

To secure end-users’ data privacy during transit, they should encrypt three things:

- The connection of their device to the web or their email provider (whether remote access to the office email or to an email-service-provider such as Gmail)
- The actual data such as email messages, chats, phone calls or text messages, and
- The stored, cached, or archived data on their devices

##### 6.2.i Encrypt Internet Connection #####

If staff leave the connection from their device unencrypted while checking email messages or the web, potential hackers sniffing this connection can easily capture their email login credentials, web traffic and any messages they send or receive. This hazard typically arises when they use an unsecured, public network (the Wi-Fi hotspot in a cafe or at the airport).

- Educate users on the risks of connecting to unsecured, public wifi connections; how to identify a secure connection (https) and train them on establishing a SSL-connection to the internet or email service by using a VPN such as Psiphon.
- Enable WAP2 to encrypt the wifi connection in the office. For added security, set up a segregated wifi connection for guest versus staff (Refer to chapter 7 - Network Security for best practices in
securing wifi).
- Installing browser plug-ins such as HTTPS-Everywhere forces the browser to use encryption on popular websites that usually aren't encrypted, thus making the web more secure. Look for https in the URL to know for sure that a site is secure. [^email_settings]

![HTTPS Icon](images/ssl_gmail.png)

Most email clients such as (Microsoft Outlook) have built-in settings [^email_settings] to ensure a secure encrypted connection is established, enable these settings during the configuration of the email client on their devices.

![HTTPS Email checkbox](images/SSL_email.png)

##### 6.2.ii Encrypt Email Messages #####

With the connection encrypted, it's time to ensure that the contents of the message are protected as well. This is especially true when using email-service-providers such as Gmail, but should also be applied when email is hosted in-house for additional user data privacy considerations. This step would ensure that system administrators are not able to read the contents of a user’s email, even though the metadata (to-from info, email subject, date-time) associated to these messages is visible.

Encrypting email messages requires creation of public & private keys for that email address. Educate users on how encryption works, setup their email clients (such as Thunderbird or Microsoft Outlook), train them on how to exchange their public key with other users, verify fingerprint on keys and create a process for them to backup their own keys. (Refer to Security-in-a-Box for step-by-step instructions)

While backing up their data, encourage users to encrypt their email or files before storing them on removable media (USB, external HDD or pushed to a cloud storage service).

![Windows File Encryption](images/win_file_encryption.png)

##### 6.2.iv Encrypt Chats, Phone Calls and Texts #####

To safeguard information exchanged via instant messages (chats), encourage staff to use Pidgin with OTR. To prevent eavesdropping on phones calls and SMS exchanges over surveilled telecommunication carriers, a variety of open-source tools such as TextSecure (Android), RedPhone (Android), Signal (iOS) by Open Whisper Systems are recommended.  Bear in mind, though, that end-to-end encryption will only exist in conversations with other TextSecure/RedPhone/Signal users, though you'll be informed when a conversation is insecure.

Some of other options to increase security include scanning encryption keys in-person with contacts to prevent man-in-the-middle attacks. In addition to training users to sending messages via data by default rather than SMS (text messages) to avoid storing metadata with your cellphone provider.

For complete guidance on helping users secure their communications, refer to [Security-in-a-Box’s guide.](https://securityinabox.org/en/guide/secure-communication)


#### 6.3 Anonymity During Surfing ####

An end-user’s unique scenario, with its associated threats and adversaries, may warrant use of anonymous web browsing. This would entail setting up the “Tor” browser (https://www.torproject.org) on their device and educating them on use, browser performance and the potential risks of Tor installed on their device based on laws & regulations specific to their scenario. Refer to [Security-in-a-Box's guide on digital shadows](https://securityinabox.org/en/guide/anonymity-and-circumvention) and [anonymous browsing](https://securityinabox.org/en/guide/torbrowser/windows) for step-by-step instructions.

#### 6.4 Preventions Against the Internet of Things (IoT) ####

With shoes recording our steps during a workout and watches monitoring our heart rate, smart devices have tightly integrated into our daily lives. And by design, they have access to our personal information such as location, contacts, photos & in some cases, even emails. Its hard to truly evaluate the private data that these device providers and apps are collecting. As the consumer market continues to get flooded with even more smart devices, its imperative to discuss this new expanded “information ecosystem” with your end-user and discuss measures they need to put in place to ensure their data privacy.

For Mobile security, refer to Security-in-a-Box’s guides on phone security:

- [https://securityinabox.org/en/guide/mobile-phones](https://securityinabox.org/en/guide/mobile-phones)
- [https://securityinabox.org/en/guide/smartphones](https://securityinabox.org/en/guide/smartphones)

#### 6.5 Reading the “Fine Print” #####

Help create a holistic security environment for users by educating them on reviewing “terms and conditions”, especially as they related to their data and its privacy and security, when signing up for tech services (email, social network sites or cloud services), smart devices or when downloading apps.

###Training Curriculum###
Refer to the suggested modules below for training on concepts outlined in this chapter

- [Level-Up: Anonymity During Surfing](https://www.level-up.cc/leading-trainings/training-curriculum/anonymity-circumvention)
- Level-Up: *Module on Encrypting User Data at Rest coming soon*
- Level-Up: *Module on Encrypting User Data in Transit coming soon*
 

###Tools & Templates###

- [Anonymous web browsing](https://www.torproject.org/)
- [Secure Email & mailing lists: Riseup.net](https://help.riseup.net)
- Encrypted cloud data storage: SpiderOak, all data on servers is encrypted and cannot be viewed by the sysadmins.
- Secure Text Messaging Apps: TextSecure, Signal, Telegram
- Encrypted phone calls: Redphone, Signal, Ostel
- [Secure web browsing: HTTPS everywhere](https://www.eff.org/https-everywhere)
- [SparkleShare.org File Synchronization](http://sparkleshare.org/)

###Recommended Reading###

- [Internews, SpeakSafe](https://speaksafe.internews.org/)
- [Tactical Tech's Security-in-a-Box](https://securityinabox.org/en)
- [Frontline Defenders: Practical Steps for Human Rights Defenders at Risk](https://www.frontlinedefenders.org/files/workbook_eng.pdf)
- [Internews, SaferJourno](https://saferjourno.internews.org/)
- [Frontline Defenders, Digital Security and Privacy for Human Rights Defenders](https://www.frontlinedefenders.org/esecman/)
- [BetterCrypto.org, Applied Crypto Hardening](https://bettercrypto.org/static/applied-crypto-hardening.pdf)

###Chapter References###

- [Wired, March 2015](http://www.wired.com/2015/03/iphone-app-encrypted-voice-texts/)
- [GizMag, Apps to easily encrypt your text messaging and mobile calls](http://www.gizmag.com/secure-text-messaging-phone-clients-comparison-ios-and-android/34000/)
- [LiUtilities, How to Encrypt a Wireless Router](http://www.liutilities.com/how-to/encrypt-a-wireless-router/)
- [OnGuardOnline.Gov, Securing Your Wireless Network](http://www.onguardonline.gov/articles/0013-securing-your-wireless-network)
- [CSOOnline, Full Disk Encryption Dos and Don'ts](http://www.csoonline.com/article/2124486/data-protection/full-disk-encryption-dos-and-don-ts.html?page=2)
- [PCWorld, How to encrypt your email](http://www.pcworld.com/article/254338/how_to_encrypt_your_email.html)
- [OnGuardOnline.Gov, Tips for Using Public Wi-Fi Networks](http://www.onguardonline.gov/articles/0014-tips-using-public-wi-fi-networks)
- [National Network to End Domestic Violence](http://tools.nnedv.org/tipsheets-charts)
- [Internews, SpeakSafe](https://speaksafe.internews.org/)
- [Tactical Tech, Security-in-a-Box](https://securityinabox.org/en)
- [FrontlineDefenders, Practical Steps for Human Rights Defenders at Risk](https://www.frontlinedefenders.org/files/workbook_eng.pdf)
- [Internews, SaferJourno](https://saferjourno.internews.org/)
- [Frontline Defenders, Digital Security and Privacy for Human Rights Defenders](https://www.frontlinedefenders.org/esecman/)
