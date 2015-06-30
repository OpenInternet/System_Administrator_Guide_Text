##Data Security, Backup and Recovery##

##Best Practices##

**8.1 Understand the data & processes**

As you design systems to protect your organization and user’s data, understand the flow of information, along with the various categories. Once you have identified the various categories of data (emails, documents, employee records, tax & other legal records, contacts, chats), create a tiered system to classify data based on its importance and sensitivity. Access to sensitive data should be limited via “Access Control” (Refer to Chapter 7 on Network Security). 

Understanding the business process of how information is created and stored at the various stages (for example: in a newsroom, information received from sources is ultimately cumulated & shared across the organization to produce a news story - the number of hands through which this information is passed from the reporter, to the page layout designer, to the editorial team) will help you design the appropriate data storage and security solutions for each stage. 

In addition, understanding the pressures & dependencies that staff deal with (such as, tight deadlines) is also imperative while proposing practical, workable data solutions that will succeed within the context of the organizational information workflow. 

**8.2 Data Collection Protocol**

As you understand the data your organization collects and creates, partner with decision-makers to understand the requirements behind collecting and storing of Personal Identifiable Information (PII). This may be personal & confidential of your organization’s donors such as bank account information and address of individual donors or birthdates of consultants. Its imperative to work with decision-makers to ensure internal policies (human resources forms, employee records, reports from implementation partners) are refined such that your organization is not collecting any more information on people than is absolutely necessary. Collecting less PII (Personal Identifiable Information) reduces the risk of data leaks and subsequent, reputational damage to your organization. 

In addition, based on your organization’s Risk Assessment (Refer to Chapter 1), if its imperative to protect the identify of staff, partners or donors working with your organization, be sure their photos or contact information is not displayed on your organization’s website. 

**8.3 Data Backup & Recovery**

*Backup Strategy* 


Based on the classification of data (emails, documents, employee records, tax & other legal records, contacts, chats) across the organization and the sensitivity assigned to each data set, you may create a backup plan that aligns with your organization’s need and the allocated data sensitivity. 

A good backup plan = encryption + the 3-2-1 rule 
The 3-2-1 rule means that the best way to backup your data is to:
- Have three copies (original files + two other copies).
- Keep them at two locations.
- One of those locations needs to be off-site (away from the office).

The purpose of this system it to make sure that you have one copy handy in emergencies, but a second copy somewhere else in case of confiscation or a natural disaster at one location. Encrypting those backups keeps the information safe on the backup, as well. 

In addition, a backup plan should: 
- Verify that remote employees are reminded to backup critical files from their PCs to a specified user share on the network which is included in the backup strategy regularly (for example, weekly or monthly).
- Verify that backups jobs (in an automatic and/or manual fashion) are performed per schedule and properly labeled.
- Verify that backup media (for example, tapes, diskettes, source code) are stored in a physically secure location, both onsite and offsite on a regular basis. (Refer to Chapter 10 on Physical Security)
- Verify that the backup media is kept in a fireproof safe or other tamper-proof/element resistant mechanism.
- Data and system restorations from backup tapes are tested in preparation of an emergency. 

Below is a typical tape backup rotation strategy, however, you may adopt a more aggressive approach of more frequent backups and segregated tapes for sensitive data as part of your backup plan. 

Typical Tape Backup Rotation Strategy
- To conserve tapes, maintain simplicity and insure sufficient retention of history, a five-day tape rotation schedule should be implemented using a different tape for each day of the week and each Friday (week-ending). Weekday tapes are retained for one month. 
- The tape used on the last day of the month is rotated out of service and retained for 12 months. At the end of each year, the tape used on the last backup of the year is rotated out and retained indefinitely. Using this schedule, any file that is stored longer than one day, but not past Friday backup, will be recoverable if restore is requested within five business days of creation date.
- If the file is recorded in a Friday backup, but not month-end, the file is recoverable if requested within 20 business days.
- If the file is recorded on a month-end backup, but not year-end backup, the file is available for recovery for approximately up to one year from creation date.
- Files that are recovered on year-end backups will be recoverable indefinitely based upon the retention duration of year-end tapes.

*Disaster Recovery*


The goal of backing-up data is to be able to plan against catastrophic data loss or accidental deletion. In the event of such scenarios, a Disaster Recovery plan can be instrumental in reducing the damage caused and will allow for uninterrupted business continuity. 
A disaster recovery plan should include:
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

Don’t wait until a disaster to test out your Disaster Recovery plan: Frequent evaluation of the disaster recovery plan is critical to ensure they adequately meet business requirements. Ensure specific procedures are in place to adequately review recovery procedures including:
- Assignment of responsibility to review and update the recovery plan to ensure that all copies reflect current conditions, including timely review and approval by appropriate levels of management.
- Authorized distribution list for contingency plans.
- The ability to recover at an alternate site.
- The ability to reconstruct systems from backups.

