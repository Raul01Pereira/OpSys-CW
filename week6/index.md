---

layout: default

title: Week 6 – System Performance Testing and Analysis

---



\## Overview

This week focuses on evaluating system performance under controlled workloads. Performance metrics for CPU, memory, disk I/O, and network activity were measured using standard Linux benchmarking and monitoring tools. The objective is to observe system behaviour under load and identify potential bottlenecks.



All tests were executed remotely via SSH using command-line tools.





Baseline System Metrics



Baseline measurements provide insight into normal system behaviour without artificial load. These metrics are used to compare against results obtained during stress testing.





A) CPU Performance Testing

CPU under stress testing was used to evaluate processor utilisation and scheduling behaviour under load. During execution, CPU usage increased significantly while system responsiveness was maintained.

!\[CPU stress test](../assets/images/week6/stress-ng.png)

\*Figure 1: CPU stress testing using stress-ng, with real-time CPU utilisation observed using top.\*







B) Memory Performance Testing

Memory stress testing was performed to observe memory allocation, usage, and paging behaviour. The results demonstrate how the operating system manages memory pressure and virtual memory resources.

!\[Memory stress test](../assets/images/week6/vmstat-stressng.png)

\*Figure 2: Memory stress testing illustrating virtual memory activity and paging behaviour using vmstat.\*









C) Disk I/O Performance Testing 

Disk I/O testing was conducted using sequential write workloads to measure storage throughput. Results reflect the performance characteristics of the virtualised storage environment.

!\[Disk I/O test](../assets/images/week6/fio.ng.png)

\*Figure 3: Disk I/O performance measured using fio, showing sequential write throughput.\*







D) Network Performance Testing

Network performance testing measured the achievable throughput between the workstation and server systems. Results demonstrate network bandwidth availability and stability during sustained data transfer.

!\[Network performance test](../assets/images/week6/iperf3png.png)

\*Figure 4: Network performance testing between workstation and server using iperf3.\*





