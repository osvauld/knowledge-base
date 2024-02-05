
Pen Test the practise of simulating a criminal breach of a sensitive area in order to uncover and fix defensive failures.

## Findings
- Internal network configuration and patch management continue to provide "easy" soft targets to pe testers who can use off-the-shelf commodity attacks to escalate privileges and move laterally about the network without being detected.
- Password management and secondary controls (2fa) are severely lacking, leading to easy compromises involving both password spraying and offline cracking hashed passwords acquired during simulated breaches.
 -  Pen testers are finding significant flaws in those vpn terminators and custom web apps.
### Code reivew
reviewing the code to find vulnerability
### Internal Network Assessment
The ultimate goal of an internal network assessment is to document and demonstrate information security risks inherent in the internal network that might be compromised by insider or exploited by an attacker.
to escalate privileges from that of an external stranger to an internal superuser.

### External network assessment
seek out vulnerabilities and misconfigurations in the client's it infrastructure, but the  name suggests only really those that are visible and reachable to an externally based attacker. This map out and exploit the internet exposed exposures and vulnerabilities of the network


### Social Engineering Engagements

Social engineering engagements almost always include some email component, 


## Engagement types compared

## Inside jobs
1/4 of the engagements are inside jobs
### outside Jobs
rest

Pen test clients are more interested in external threats.

### Vulnerabilities deep dive
![[Pasted image 20240205143023.png]]

Inside Jobs
The top three most common vulnerabilites taken together is a pwoerful set of vulnerabilities that can quickly elevate an attacker to Domain Admin privileges

### Lateral movement techniques

Once a pen tester has acheived access to atleast one machine in the network, next they try to move around the network.

![[Pasted image 20240205144613.png]]

### Comparison and Use Cases

- **WMI** is deeply integrated into Windows and is more about accessing a wide range of system information and management capabilities. It's used for monitoring, information retrieval, and complex system management tasks. WMI can interact with almost any aspect of the Windows operating system.
- **PsExec** is more focused on executing processes on remote systems. It's commonly used for running commands or scripts remotely, software installation, or quick administrative tasks across networks.


### Outside Jobs

![[Pasted image 20240205145313.png]]
### Electronic Social Engineering(ESE)

Email based electronic social engineering: what happend?

![[Pasted image 20240205151110.png]]
many advanced external engagements involve electronic social engineering. These mostly involve "layer 8" (aspects of human interactions and tendencies like trust feat or greed) there is still an significant technological components to such attack


DMARC, which stands for Domain-based Message Authentication, Reporting, and Conformance, is an email authentication protocol designed to give email domain owners the ability to protect their domain from unauthorized use, commonly known as email spoofing.


The most common payload fro a ese attack is to direct users to an attacker controlled website much more common than delivering malware.


The second most popular way to collect usernames from the outside is through website enumeration, which is when a web application gives away information on what is a valid username and what isn't

#### **Purloining Passwords** 
Password spraying, in which the attacker already knows of a list of valid usernames, but tries only a few of very special unoriginal passwords. 

### Hacking Hashes

![[Pasted image 20240205205516.png]]
Some password hashes are easily crackable
![[Pasted image 20240205205657.png]]
truly strong passwords are rare in a given hashfile, we can slo confim that people pick very guessable predicable passwords.

![[Pasted image 20240205210035.png]]
### Lockout policies 

most companies dont have them.

2fa was not enabled most of the time.

#### **Securing Credentials**

The best defense against both password spraying and protecting the contents of hashfiles from commodity cracking is, somewhat surprisingly, the same: Don't rely on humans to pick passwords

The one program any IT organization can take on to best enhance the security of their organization would be to standardize on **machine-controlled password management**.


## Detection,Response and Defense.

- **Review your password management strategy.** So many penetration tests end up with lists and lists of poorly chosen, human-generated passwords, regardless of whatever other fancy security controls are in place. Credential management can, and should, be a full-time function of an organization's IT security program, and the more users and services that can be moved to automatically generated, automatically rotated passwords, the better. It can be painful at first to adopt machine-controlled password management, but after a while, it will become second nature. Training and supporting users in the use of password management solutions will make them all but impervious to accidentally leaking passwords through social engineering, as well as render a purloined NTDS.dit hash file all but useless.
- **Review your patch management strategy.** The best use of an internal network assessment is to figure out where your patch management strategy is failing—what dark, cobwebby corners of your IT infrastructure aren’t getting routine reviews for patches and updates. If an enterprise is relying on the users to do the right thing and click through those nag screens for updates (instead of hitting "later" again and again, forever), your penetration testers will almost certainly be overwhelmed with so many exploitable vulnerabilities that you'll only hear about the most egregious examples of where individual people have failed to keep up on updates.
- **Employ network segmentation wherever possible.** Small, manageable network segments can do worlds of good when it comes to containing an internal breach. Penetration testers spend a fair amount of time and energy not so much on getting that first shell, but in deciding where to go next. Big, flat networks can present hundreds of opportunities for lateral movement, and also tend to be difficult to manage with expensive D&R programs. The name of the game here is to bottle up attackers, both criminals and penetration testers, and make it difficult to move from asset to asset in search of systems that are both compromisable and useful launching points for the next compromise.