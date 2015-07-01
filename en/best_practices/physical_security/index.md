##Physical Security## 
{#chapter10}

While monitoring network traffic to prevent virus & malware attacks and
ensuring data and communication security are important aspects of a
System Administrator’s job, it’s equally imperative to prevent physical
damage and access to your organization's infrastructure.

###Best Practices###

#### 10.1 Equipment Security ####

Create an inventory (such as, a secured, encrypted database) of all
organizational equipment. Place serial numbers on all hardware (servers,
monitors, computers, laptops, external hard drives, keyboards, recording
devices etc). Create a “check-out/check-in” procedure for devices (such
as such as phones, laptops, and headsets) that need to be borrowed
during work travel.

#### 10.2 Prevent unauthorized access to your ISP connection ####

Ensure internet cables connections from your ISP (internet service
provider) cannot be tampered with. Usually these cables terminate in a
main “electrical/telecommunications” closet in your office building;
make sure physical access to this closet is authorized and monitored.
Always escort a representative from the ISP or local telecommunications
provider when providing physical access to this electrical closet.

#### 10.3 Prevent unauthorized physical access ####

- Physical security of your organization starts at your building’s doorstep. This includes who the building security guard allows access to, followed by authorization to enter the office premises after approval from the receptionist. Ensure that your organization has a guest entry log procedure. All non-employees should be escorted by a staff person present at all times, including any service providers.
- If the situation warrants it (based on your organizational Risk Assessment - Chapter 1) and after consultation with the organization’s decision-makers, consider installing security cameras to monitor the office premises. Make sure signs informing staff & visitors that they are being “surveilled” via these cameras are clearly placed to ensure complete transparency. In addition, ensure that the cameras are installed such that they won’t invade privacy of staff by capturing their computer screens; create a policy that communicates secure storage & access of the security camera tapes. the At the very least, there should be a procedure in place to safeguard the premises via an alarm system or access to the office keys by critical staff. If keys are used to secure premises, ensure that keys are handled securely at all times and there is a key handling policy in place.
- Locate critical networks, servers, workstations and telecommunications equipment in physically secure locations that permit access only to authorized personnel.[^physical] Consider investing in locked closets to provide additional security and have clear signs denoting areas of unauthorized access to staff. Always accompany a vendor in the server room if service is being received.
- Ensure servers are mounted on sturdy racks, a few feet above the ground. Cables should be clearly marked and secured above ground, not left loose as this could be hazardous to staff.[^physical_security]
- WAPs (wifi access points) should be secured via in a sealed, transparent “security box” ensuring that they cannot be tampered with.
- In addition to protecting servers, routers, WAP(s), ensure that the office phone sets, fax stations, scanners and printers are equally secured and access is restricted to staff. These devices should be placed in visible common areas to prevent tampering.  Place reminders next to fax machines and printers to ensure staff are not leaving sensitive documents unattended and all confidential documents are shredded before they are disposed.
- Ensure your office’s facilities - main power supply, internet connection from the ISP (internet service provider), air conditioning and UPS (Uninterruptible Power Supply) cannot be tampered with. Its recommended to have backup UPS powered and ready to go in case of device failure of the main UPS for critical IT services. Where feasible, you may also consider a redundant power supply (such as a generator) or internet connection (a backup ISP). Take into account costs associated to ensuring redundancy & business continunity. (Refer to Chapter 4-Budegting for Security and Chapter 8-Data Security, Backup & Recovery for additional best practices)
- Invest in fire extinguishers for the office, and in particular for the server room. Consider investing in gas-based fire extinguishers that wont damage servers or other equipment in the server room. Display a clearly marked fire escape plan in common areas and in the server room.
- Secure all desktops, laptops and other portable devices with locks.


#### 10.4 System Console & Auto-logout ####

The system console should be physically protected. If there is physical
access to system console and the computer, it is easy for anyone to
break-in or misuse. Most of the systems have backdoor entry or procedure
to break into the system, using the console. In fact, this is an
essential feature to break into the system when the superuser password
is lost. Secure your console from someone who can keep guessing the
superuser password at the console, as recommended in SANS Institute's guide [^systemconsole] on System Administration Security Practices:

-   Do not leave console logged in at any point of time, if you are
    away; make a practice to log-out every time after completing your
    job. If your system supports timeout feature for system console,
    configure it.
-   System administrators generally have an habit of keeping multiple
    sessions/windows to different systems simultaneously active to carry
    out administrative tasks. If an intruder breaks into a system
    administrator's terminal, there is a chance of getting access to
    multiple systems. These terminals should be located in a secure
    area.[^systemconsole]
-   Evaluate a policy for remote access to servers: while this can be
    added convenience for system administrators, if not implemented and
    monitored carefully, it can also expose a huge security hole into
    your organization’s infrastructure. If possible, disable remote
    access to better manage risks. However, in case remote access is
    enabled, ensure you use an encrypted VPN channel (such as Psiphon,
    RiseupVPN) to connect to your organization’s servers.

#### 10.5 Loss of physical access to the office/server room ####

In case of an emergency, when you are unable to physically access the
server room due to a natural calamity or political discord (riots or
curfew), ensure you have a communication plan in place to communicate
with staff and have have a tested data recovery strategy in place (Refer
to Chapter 8 on Data Security, Backup & Recovery). Ensure that backup
tapes are stored in secure locations - it is considered best practice to
secure tapes in 2 distinct locations to create another layer of physical
security for your backups. All tapes should be encrypted to prevent data
loss in case of theft or confiscation.

#### 10.6 Know your rights ####

During an office raid, be aware of local laws and your rights before
allowing physical access to your organization's infrastructure to local
law enforcement. In collaboration with your organization’s lawyers &
decision-makers, understand what data can & cannot be handed over to
local authorities without a warrant.

Stage a “mock office raid” to evaluate physical loss of data
(confiscation of computers, servers, phones, cameras, files & records in
paper format) and evaluate gaps in the physical security of your
organization to plan next steps.

After considering the risks, consider partnering with like-minded
organizations to create a digital *“panic button”*. This could a simple
solution of creating a messaging group for sending a SMS (or tweet) to a
select group of people, a contact at the embassy (in case of
international NGOs), or other community organizations to alert external
sources and in some cases, even the local media, that your
organization’s rights are being violated during an office raid. Raising
awareness of your organization’s situation could allow legal aid, human
rights & independent media advocates, and in some cases, even the
international community, to rally for your organization’s rights.

#### 10.7 Know thy neighbor ####

As an organization focused on human rights or an independent media
outlet, it's important for you to be aware of your physical location
vis-a-vis your adversaries and be conscious of other groups in your
neighborhood or office building. These considerations are especially
important when leasing office space. While leasing office space close to
other human rights groups may create a community of like-minded
organizations in the same neighborhood leading to a sense of solidarity,
it could also raise visibility (and possible scrutiny by local law
enforcement) of your organization based on the media attention received
by your neighbors. Assess and re-evaluate your physical security plan
based on these external factors regularly.

#### 10.8 Healthy environment for your hardware ####

Like many electronic devices, computers are quite sensitive. They do not
adapt well to unstable electricity supplies, extreme temperatures, dust,
high humidity or mechanical stress. There are a number of things you can
do to protect your computers and network equipment from such threats, as suggested in Tactical Tech's Security-in-a-Box guide [^healthy_environment]:

-   Electrical problems such as power surges, blackouts and brownouts
    can cause physical damage to a computer. Irregularities like this
    can crash your hard drive, damaging the information it contains, or
    physically harm the electronic components in your computer. Invest
    in a UPS (Uninterruptible Power Supplies) to stabilise electricity
    supply and provide temporary power in the event of a blackout.
-   Test your electrical network before you connect important equipment
    to it. Try to use power sockets that have three slots, one of them
    being a 'ground line', or 'earth'. And, if possible, take a day or
    two to see how the electrical system in a new office behaves when
    powering inexpensive devices, such as lamps and fans, before putting
    your computers at risk.
-   To defend against accidents in general, avoid placing critical
    hardware in passages, reception areas or other easily accessible
    locations.
-   UPS', power filters, surge protectors, power strips and extension
    cables, particularly those attached to servers and networking
    equipment, should be positioned where they will not be switched off
    by an accidental misstep.
-   If you keep any of your computers or servers inside cabinets, make
    sure they have adequate ventilation, or they might overheat.
-   Computer equipment should not be housed near radiators, heating
    vents, air conditioners or other ductwork.
-   Exposed power strips or wires are a fire hazard; keep cables away
    from water or direct sunlight.

###Tools & Templates###

- VPN: [Psiphon](https://psiphon.ca/); [RiseupVPN](https://help.riseup.net/en/vpn)

###Recommended Reading###

-   [NIST, Physical and Environmental Security](http://csrc.nist.gov/publications/nistpubs/800-14/800-14.pdf)
-   [Security-in-a-box:](https://securityinabox.org/en/guide/physical)
-   [Frontline Defenders, Workbook on Security](http://frontlinedefenders.org/files/workbook\_eng.pdf\#page=80)
-   [TechRepublic, 10 physical security measures every organization should take](http://www.techrepublic.com/blog/10-things/10-physical-security-measures-every-organization-should-take/)
-   [SANS Institute, Data Center Physical Security Checklist](http://www.sans.org/reading-room/whitepapers/awareness/data-center-physical-security-checklist-416)
-   [Frontline, Protection Manual for Human Right Defenders](http://www.peacebrigades.org/fileadmin/user\_files/groups/uk/files/Publications/Frontline\_Manual\_pdf.pdf\#page=83)
-   [Pentest Standard](http://www.pentest-standard.org/index.php/Pre-engagement\#Physical\_Penetration\_Test)


###Chapter References###

-   [SANS Institute, System Administrator - Security Best Practices](http://www.sans.org/reading-room/whitepapers/bestprac/system-administrator-security-practices-657)
-   [SANS Institute, Computer Rooms - meet the physical security measures](http://www.giac.org/paper/gsec/2892/computer-rooms-meet-physical-security-measures/104866)
-   [University of Florida, Physical Security of Server Rooms](https://security.ufl.edu/wp-content/uploads/2013/09/PS0002-02.pdf)
-   [MIT, Protecting Devices](https://ist.mit.edu/security/devices)
-   [Tactical Tech, Security-in-a-Box](https://info.securityinabox.org/default/chapter\_2\_3)
-   [SANS Institute, Penetration Tests and Red Team Exercises](https://www.sans.org/critical-security-controls/control/20)
