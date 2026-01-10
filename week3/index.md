
---
layout: default
title: Week 3 – Application Selection for Performance Testing
nav_order: 3
---

## Overview



This week focuses on selecting representative applications that generate different types of system workloads. These applications will be used in later phases to evaluate operating system performance under varying conditions, including CPU, memory, disk I/O, and network usage.







\## Application Selection Strategy



To analyse operating system behaviour effectively, applications were chosen to represent distinct workload categories. Each application targets specific system resources, allowing meaningful performance comparisons and bottleneck identification.



---



\## Application Selection Matrix



| Application | Workload Type | Resource Focus | Justification |

|------------|--------------|----------------|---------------|

| stress-ng | CPU-intensive | CPU | Generates controlled CPU load to analyse scheduling behaviour and utilisation |

| stress-ng | Memory-intensive | RAM | Simulates memory pressure to evaluate allocation and paging behaviour |

| fio | I/O-intensive | Disk I/O | Measures disk throughput, latency, and IOPS |

| iperf3 | Network-intensive | Network | Tests network throughput and latency |

| nginx | Server workload | CPU, Network | Represents a real-world web server workload |



---



\## Installation Documentation



All applications were installed remotely via SSH using the system package manager.



\### stress-ng

```bash

sudo apt update

sudo apt install stress-ng



\## fio

sudo apt install fio





Selecting applications based on workload characteristics ensures structured and meaningful performance analysis. This approach enables clear identification of operating system behaviour under stress and provides a strong foundation for quantitative performance evaluation and optimisation in subsequent weeks.

