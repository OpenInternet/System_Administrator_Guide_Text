##Data Security, Backup and Recovery## {#chapter8}

###Best Practices###

#### 8.1 Understand the Data & Processes ####

As you design systems to protect your organization and user’s data, understand the flow of information, along with the various categories. Once you have identified the various categories of data (emails, documents, employee records, tax and other legal records, contacts, chats), create a tiered system to classify data based on its importance and sensitivity. Access to sensitive data should be limited via “Access Control” (Refer to Chapter 7 on Network Security).

Understanding the business process of how information is created and stored at the various stages (for example: in a newsroom, information received from sources is ultimately cumulated and shared across the organization to produce a news story - the number of hands through which this information is passed from the reporter, to the page layout designer, to the editorial team) will help you design the appropriate data storage and security solutions for each stage.

In addition, understanding the pressures and dependencies that staff deal with (such as, tight deadlines) is also imperative while proposing practical, workable data solutions that will succeed within the context of the organizational information workflow.

#### 8.2 Data Collection Protocol ####

As you understand the data your organization collects and creates, partner with decision-makers to understand the requirements behind collecting and storing of Personal Identifiable Information (PII). This may be personal and confidential of your organization’s donors such as bank account information and address of individual donors or birthdates of consultants. Its imperative to work with decision-makers to ensure internal policies (human resources forms, employee records, reports from implementation partners) are refined such that your organization is not collecting any more information on people than is absolutely necessary. Collecting less PII (Personal Identifiable Information) reduces the risk of data leaks and subsequent, reputational damage to your organization.

In addition, based on your organization’s Risk Assessment (Refer to Chapter 1), if its imperative to protect the identify of staff, partners or donors working with your organization, be sure their photos or contact information is not displayed on your organization’s website.

#### 8.3 Data Backup & Recovery ####

**Backup Strategy**

Based on the classification of data (emails, documents, employee records, tax and other legal records, contacts, chats) across the organization and the sensitivity assigned to each data set, you may create a backup plan that aligns with your organization’s need and the allocated data sensitivity.

A good backup plan = encryption + the 3-2-1 rule

The 3-2-1 rule means that the best way to backup your data is to:

- Have three copies (original files + two other copies).
- Keep them at two locations.
- One of those locations needs to be off-site (away from the office).

The purpose of this system it to make sure that you have one copy handy in emergencies, but a second copy somewhere else in case of confiscation or a natural disaster at one location. Encrypting those backups keeps the information safe on the backup, as well.

In addition, a backup plan should [^backup]:

- Verify that remote employees are reminded to backup critical files from their PCs to a specified user share on the network which is included in the backup strategy regularly (for example, weekly or monthly).
- Verify that backups jobs (in an automatic and/or manual fashion) are performed per schedule and properly labeled.
- Verify that backup media (for example, dvds, tapes, diskettes, source code) are stored in a physically secure location, both onsite and offsite on a regular basis. (Refer to Chapter 10 on Physical Security)
- Verify that the backup media is kept in a fireproof safe or other tamper-proof/element resistant mechanism.
- Data and system restorations from backup media are tested in preparation of an emergency.

Below is a typical tape backup rotation strategy, however, you may adopt a more aggressive approach of more frequent backups and segregated tapes for sensitive data as part of your backup plan.

**Typical Removable Media (tapes, DVDs) Backup Rotation Strategy** [^backup]

- To conserve backup media, maintain simplicity and insure sufficient retention of history, a five-day incremental rotation schedule should be implemented using a different media for each day of the week and each Friday (week-ending). Weekday media are retained for one month.
- The media used on the last day of the month is rotated out of service and retained for 12 months. At the end of each year, the media used on the last backup of the year is rotated out and retained indefinitely. Using this schedule, any file that is stored longer than one day, but not past Friday backup, will be recoverable if restore is requested within five business days of creation date.
- If the file is recorded in a Friday backup, but not month-end, the file is recoverable if requested within 20 business days.
- If the file is recorded on a month-end backup, but not year-end backup, the file is available for recovery for approximately up to one year from creation date.
- Files that are recovered on year-end backups will be recoverable indefinitely based upon the retention duration of year-end media.

**Disaster Recovery**

The goal of backing-up data is to be able to plan against catastrophic data loss or accidental deletion. In the event of such scenarios, a Disaster Recovery plan can be instrumental in reducing the damage caused and will allow for uninterrupted business continuity.

A disaster recovery plan [^backup] should include:

- Identification of critical systems, application data and programs, equipment, communications requirements, documentation, and supplies. Identify interdependencies of these systems between your organization’s business units or functions.
- Risk analysis for each data set including impact analysis (impact on organization productivity, continuity, reputation), acceptable downtime and disaster definition.
- Prioritized tiers to approach recovery based on risk analysis - this includes data and application software (for example: restore email before contact management system)
- Key users and vendor personnel should be identified.
- Various levels of disruption should be identified - full, software-failure, hardware-failure, and database corruption.
- Documented scenarios for each level of disruption including specific procedures and assignment of responsibilities (in case of more than one system administrator) should be defined. Procedures should include steps reinstallation of data and programs, including any dependencies. (Refer to Chapter 7 on good documentation)
- Retention of source documents and re-input of data in case of database failure.
- Security requirements for alternate processing environment should be defined, in case of physical damage to the office and setup at a staff’s house.
- Verify that the offsite storage facilities, including cloud infrastructure, are included in contingency plan.
- Access to vendors contracts and replacement commitments.
- Considerations for a Hot/Cold sites for critical systems: A hot site is a completely functioning alternate site in another independent geographic location complete with backup systems and a duplicate and current environment. This is the most painless way to recover from a catastrophe or calamity; however, it is certainly the most expensive. A cold site merely contains system, personnel space and the network connectivity necessary to facilitate resumption, but does not have any systems or data.

Don’t wait until a disaster to test out your Disaster Recovery plan: Frequent evaluation of the disaster recovery plan is critical to ensure they adequately meet business requirements. Ensure specific procedures [^backup] are in place to adequately review recovery procedures including:
- Assignment of responsibility to review and update the recovery plan to ensure that all copies reflect current conditions, including timely review and approval by appropriate levels of management.
- Authorized distribution list for contingency plans.
- The ability to recover at an alternate site.
- The ability to reconstruct systems from backups.

![Disaster Recovery Plan](images/disaster_recovery.png)

#### 8.4 Data Retention, Archiving and Disposal ####

Based on the classification of your organization’s data, create a Retention, Archiving and Disposal (RAD) plan. While data storage capacity is getting inexpensive in most countries, it may be prudent to create a RAD plan to avoid accidental leakage of data, reduce the risk of malicious deletion or unauthorized access.

Understand local data retention laws before disposing digital files - such as employee records, tax information. Moreover, merely deleting sensitive material is not sufficient, as it does not actually remove the data from your system.

Disposal of data also includes protocols of securely shredding physical files and documents to prevent unauthorized access to printouts of sensitive information.

#### 8.5 Contact Management Provisions ####

Contact information of people that your staff interact with (whether partners, sources, consultants, or donors) usually resides in their email or on their phones. One hacked email account on your network or a lost phone can expose the identity of these individuals putting them at risk. In addition, turnover within your organization may also lead to the loss of contact information to key individuals. As such, create provisions to provide a secure (encrypted) database to store all contact information in order to provide business continuity and safeguard the contact information of individuals by moving them away from individual email accounts or address books. Institute a contact management policy within the organization to ensure all contact information is kept up-to-date in the contact management system and sharing of contacts tagged as “sensitive” is not permissible.

Ensure that your backup policy addresses regular backups of the contact management system and the physical protection of these backups.

#### 8.6 Data Security While Crossing Borders ####

While it’s important to create provisions to protect data while on the network, be aware of various methods through which your organization’s data also travels outside the network on staff laptops, USBs or stored in the cloud by staff. As you design the organization’s Traveller's Policy (Refer to Chapter 2 on IT Policies) discuss the protocols for safeguarding your organization’s data while crossing borders (especially imperative when staff travel to “less friendly” countries).

As security provisions will be unique to each scenario, it’s important to institute a “check-in” policy with staff before they travel to design unique, but workable, data storage and security solutions based on their needs. A few simple examples could include - ensuring staff remove sensitive data from their computers and phones, or prepare a “loaner” laptop that holds the bare minimum information required for their assignment, creating a “TAILS” repo for staff to store sensitive information, understanding data loss in case the laptop or phone gets confiscated.

#### 8.7 Physical Access and Security ####

**Storage of Backup Tapes**: Ensure that all backups are properly labeled and provisions to transport them to a secure, off-site location are made. An off-site backup location may be a storage service provider or the home of the executive director or lead systems administrator.

When backups are stored at an off-site backup storage service provider, it’s imperative to understand service level agreement with this vendor and their liability to safeguard your data (Refer to Chapter 5). When backup media is stored in the home of a key stakeholder, ensure they understand the implications of safeguarding these tapes.Ensure that all backup media is kept in a fireproof safe or other tamper-proof/element resistant mechanism to prevent damage from theft, fire or floods.

Finally, verify that the offsite storage facilities for backups are included in disaster recovery/contingency plan.

**Prevention against Data Leaks**: In order to protect against “Insider Threats” of accidental data leakage, ensure there is an “Access Control” policy in place (Refer to Chapter 7 on Network Security)

**Chain of Custody**: When working with a team of system administrators, create a “chain of custody” - this details who has physical access to the data tapes at any given time. The chain of custody would also detail a “check-in/check-out” procedure for access to the backup media.

**Facility Construction**: The physical construction of the facility where your data will be stored is an important consideration as well. Plan against adverse scenarios like natural calamities such as fire, floods, or political discord (bombings, riots, curfew). Creating a disaster recovery and a communication plan will keep key stakeholders (Executive Director, Finance and HR Director) informed about the next steps in case of an emergency.

**Office Raid**: While planning against an office raid by government officials, refer to Chapter 10: Physical Security.

###Training Curriculum###
Refer to the suggested modules below for training on concepts outlined in this chapter

- [LevelUp: Data backup and recovery](https://www.level-up.cc/leading-trainings/training-curriculum/data-retention-and-backup)
- [LevelUp: Data retention, Archiving, Disposal](https://www.level-up.cc/leading-trainings/training-curriculum/data-retention-and-backup) 
- SAFETAG: Data Assessment- Sensitive Data: [English](https://github.com/OpenInternet/SAFETAG/releases/download/v0.4/SAFETAG.Full.guide.English.pdf) | [Spanish](https://github.com/OpenInternet/SAFETAG/releases/download/v0.4/SAFETAG.Full.guide.Espanol.pdf)


###Tools & Templates###

- [Backup software- Windows and Linux: Duplicati](http://www.duplicati.com/)
- [Backup for Windows: Cobian](https://securityinabox.org/en/guide/cobian/windows)
- [Secure File Storage, TrueCrypt](https://securityinabox.org/en/guide/truecrypt/windows#601)
- [Secure deletion tool - Eraser](https://securityinabox.org/en/guide/eraser/windows)
- [Windows Bitlocker](http://windows.microsoft.com/en-us/windows7/products/features/bitlocker)
- [TechTarget - IT Disaster Recovery Plan Template By Paul Kirvan, CISA, CISSP, FBCI, CBCP](http://searchdisasterrecovery.techtarget.com/feature/IT-disaster-recovery-DR-plan-template-A-free-download-and-guide)

###Recommended Reading###

- [TechRepublic, 10 things you should know about deploying a UPS](http://www.techrepublic.com/article/10-things-you-should-know-about-deploying-a-ups/)
- [TechTarget, How to choose the right uninterruptible power supply for your data center](http://searchdatacenter.techtarget.com/tip/How-to-choose-the-right-uninterruptible-power-supply-for-your-data-center)
- [NIST, Guidelines on Security and Privacy in Public Cloud Computing](http://csrc.nist.gov/publications/nistpubs/800-144/SP800-144.pdf)
- [Scott Hanselman, The Computer Backup Rule of Three](http://www.hanselman.com/blog/TheComputerBackupRuleOfThree.aspx)

###Chapter References###

- [NIST, Contingency Planning Guide for Federal Information Systems](http://csrc.nist.gov/publications/nistpubs/800-34-rev1/sp800-34-rev1_errata-Nov11-2010.pdf)
- [SANS Institute, Disaster Recovery Plan Strategies and Processes](http://www.sans.org/reading-room/whitepapers/recovery/disaster-recovery-plan-strategies-processes-564)
- [Internews, SaferJourno](https://saferjourno.internews.org)
- [ComputerWeekly, How to write a disaster recovery plan and define disaster recovery strategies](http://www.computerweekly.com/feature/How-to-write-a-disaster-recovery-plan-and-define-disaster-recovery-strategies)
- [SANS Institute, Essential Information Security](http://www.sans.org/reading-room/whitepapers/awareness/essential-information-security-corporate-employees-1179)
- [Texas A&M, Information Technology Disaster Recovery Plan](https://www.tamuct.edu/departments/informationtechnology/extras/ITDisasterRecoveryPlan.pdf)
- [Online Trust Alliance, Security & Privacy Best Practices](https://otalliance.org/resources/security-privacy-best-practices)
- [BlackStratus, 17 Best Practices for Maintaining Data Security in a Business Environment](http://www.blackstratus.com/blog/practices-maintaining-data-security-business-environment/)
- [ZDNet, Securty Best Practice Guidelines for Business](http://www.zdnet.com/article/10-security-best-practice-guidelines-for-businesses/)
- [Interactive Advertising Bureau, Data Security](http://www.iab.net/guidelines/508676/508905/data_security)
- [FoxBusiness, Data Security Best Practices](http://smallbusiness.foxbusiness.com/technology-web/2014/06/19/data-security-best-practices/)
- [Microsoft, Best Practices for Enterprise Security](https://msdn.microsoft.com/en-us/library/cc750076.aspx)
- [Microsoft, Data Security and Data Availability in the Administrative Authority](https://msdn.microsoft.com/en-us/library/cc722918.aspx)
- [DisasterRecovery.org](http://www.disasterrecovery.org/it_network_dr.html)
- [Disaster Recovery Guide](:http://www.disaster-recovery-guide.com/)
- [Indiana university](https://kb.iu.edu/d/akln)
- [Ready.gov, IT Disaster Recovery Plan](http://www.ready.gov/business/implementation/IT)
