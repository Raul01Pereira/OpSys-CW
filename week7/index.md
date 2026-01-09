---

layout: default

title: Week 7 – Security Audit and System Evaluation

---



\## Overview

This week focuses on reviewing and evaluating the security posture of the Linux server after all configuration, monitoring, and performance testing activities. A security audit was conducted to assess authentication controls, access control mechanisms, firewall rules, and overall system hardening.



The aim is to identify strengths, remaining risks, and areas for improvement, linking practical implementation to operating system security theory.







The system security configuration follows the AAA (Authentication, Authorisation, and Access Control) model. Authentication is enforced through SSH key-based login, ensuring only trusted users can access the system. Authorisation is managed through sudo privileges, limiting administrative actions to authorised users. Access control is enforced through Linux file permissions and firewall rules, preventing unauthorised resource access.







A) User and Privilege Audit

A review of user privileges confirmed that only authorised users are members of the sudo group. Routine administration is performed using a non-root account, enforcing the principle of least privilege and reducing the risk of accidental or malicious system modification.



!\[User privilege audit](../assets/images/week7/admin.png)



\*Figure 1: User privilege audit confirming that the account `cacife01` has controlled administrative access via sudo, enforcing the principle of least privilege.\*







B) SSH and Remote Access Audit 

SSH configuration was audited to verify that password authentication is disabled and root login is prohibited. These controls significantly reduce the attack surface by preventing brute-force password attacks and limiting direct privileged access.





!\[SSH service status](../assets/images/week7/ssh.png)



\*Figure 2: The SSH service is enabled and actively running, confirming that the system supports secure remote administration via an operational SSH daemon.\*



"How is SSH hardened?" The answer Figure 3. (Configuration evidence)

!\[SSH configuration audit](../assets/images/week7/sshd.png)



\*Figure 3: SSH daemon runtime configuration audit showing that password-based authentication is disabled and that root access is restricted to key-based authentication only.\*







C) Firewall and Network Exposure Review

Firewall rules were reviewed to ensure that inbound traffic is restricted by default and that SSH access is permitted only from the workstation system. This layered defence approach reduces exposure to network-based attacks and supports defence-in-depth principles.



!\[Firewall status](../assets/images/week7/ufw.png)



\*Figure 3: UFW firewall configuration enforcing a default deny policy for incoming traffic while permitting SSH access.\*









Intrusion Detection Considerations (Concept)

While no dedicated intrusion detection system (IDS) was deployed, the system configuration supports host-based monitoring through log inspection and process auditing. Linux system logs, authentication records, and process monitoring tools provide visibility into system activity and can assist in identifying anomalous behaviour.

Host-based IDS solutions monitor log files, file integrity, and process execution to detect suspicious activity, complementing preventative security mechanisms such as firewalls and access controls. A network-based IDS could further enhance detection by monitoring inbound and outbound traffic patterns.







Security Model Evaluation (DAC, MAC, RBAC)

The system primarily operates under a Discretionary Access Control (DAC) model using standard Linux file permissions and ownership. DAC provides flexibility and ease of administration but relies heavily on correct user behaviour and privilege management.

Mandatory Access Control (MAC) frameworks such as AppArmor or SELinux could further strengthen system security by enforcing system-wide policies that restrict application behaviour regardless of user permissions. While MAC improves containment and reduces the impact of compromised accounts, it introduces additional configuration complexity. In this system, DAC was considered sufficient for the scope of the deployment, with MAC identified as a potential enhancement.









Limitations and Improvements

Although the system is securely configured, several improvements could further enhance its security posture. These include deploying a host-based intrusion detection system, enabling a mandatory access control framework, and automating log analysis using custom Bash scripts.

Additional enhancements could involve enforcing stricter SSH access controls and implementing regular security audits. These measures would improve detection capabilities, reduce reliance on manual monitoring, and increase resilience against misconfiguration or compromise.









\## Reflection

This coursework demonstrated how operating system security is achieved through layered controls rather than a single mechanism. Secure authentication, controlled authorisation, and enforced access control collectively reduce risk. Performance testing highlighted trade-offs between security and usability, reinforcing the importance of balanced system design. Overall, the project strengthened the understanding of Linux system administration, security fundamentals, and performance evaluation in real-world environments.



