\# Week 1 - System Planning



\## Distribution Selection



\*\*Chosen Distribution:\*\* Ubuntu Server 25.10



\### Justification

Ubuntu Server 25.10 was selected to provide access to newer kernel features and system utilities, supporting experimentation and learning within a controlled virtualised environment. Although this is not a Long-Term Support (LTS) release, it was deemed acceptable for this coursework as the focus is on operating system configuration, command-line administration, security concepts, and performance evaluation rather than long-term production stability.



Ubuntu provides strong documentation, an active community, and widespread industry adoption, making it suitable for learning modern Linux server administration.



\### Alternatives Considered

\- \*\*Ubuntu Server 22.04 LTS:\*\* Offers long-term stability but fewer recent features

\- \*\*Debian:\*\* Highly stable but slower update cycle

\- \*\*CentOS Stream:\*\* Rolling-release model is less predictable for structured coursework



Ubuntu Server 25.10 provides a balance between modern features and usability within an academic environment.



* Gained an understanding of Linux server architecture and headless system design.
* Learned how to gather system and hardware information using command-line tools.
* Developed familiarity with SSH-based remote administration.





\### Key Learning Outcomes (Week 1)



* Operating systems play a critical role in sustainable computing by acting as intermediaries between hardware resources and user applications. Efficient OS design enables better CPU scheduling, memory management, and I/O control, which directly reduces energy consumption and improves overall system efficiency.



* The separation between user space and kernel space enhances system stability and security, allowing controlled access to hardware resources through system calls. This architectural design supports both performance optimisation and reduces system overhead.



* Modern computing environments, particularly data centres, consume a significant and growing proportion of global electricity. Operating system features such as virtualisation support, power management, and efficient resource allocation help improve hardware utilisation and reduce environmental impact.



* This week highlighted the trade-offs between performance and energy efficiency, demonstrating how operating systems must balance responsiveness, resource usage, and sustainability when managing modern computing systems.





Architecture diagram.



!\[System Architecture Diagram](..assets\\diagrams\\architecture-week1.png)





System Specifications.



\### Kernel and OS Information.

!\[Kernel Information](../assets/images/uname-a.png)

!\[Distribution Information](../assets/images/lsb-release.png)



\### Memory Usage.

!\[Memory Usage](../assets/images/free-h.png)



\### Disk Usage.

!\[Disk Usage](../assets/images/df-h.png)



\### Network Configuration.

!\[Network Configuration](../assets/images/ip-addr.png)

