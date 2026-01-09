
---

layout: default
title: Week 2 – System Architecture and Linux Foundations

---


# Week 2 – System Architecture and Linux Foundations

## Overview
This week focused on understanding the internal architecture of operating systems and the foundational components of Linux systems. Theoretical concepts such as kernel design, layered architecture, and the boot process were explored alongside essential command-line tools used for system administration. This knowledge provides the foundation for later security configuration and performance analysis tasks.



## Operating System Architecture

An operating system is structured in layers to separate user applications from hardware resources. This layered approach improves system stability, security, and maintainability by controlling how software interacts with hardware.

### Kernel Architectures

Monolithic Kernel  
In a monolithic kernel, most operating system services run in kernel space, including device drivers, file systems, and process management. This design offers high performance but increases the attack surface and complexity. Linux uses a monolithic kernel architecture.

**Microkernel**  
A microkernel keeps only essential services in kernel space, such as inter-process communication and scheduling. Other services run in user space, improving isolation and fault tolerance at the cost of performance overhead.

**Hybrid Kernel**  
Hybrid kernels combine aspects of monolithic and microkernel designs by keeping performance-critical components in kernel space while isolating others. Examples include Windows NT and macOS.

Linux’s monolithic kernel design is well-suited for server environments where performance efficiency is a priority.

---

## Layered Architecture and System Calls

Operating systems separate functionality into layers, typically consisting of user applications, system libraries, the system call interface, the kernel, and hardware. User applications cannot directly access hardware and must request services through system calls.

System calls act as a controlled gateway between the user space and kernel space, ensuring security and stability by preventing unauthorised access to hardware resources.

---

## Boot Process

The Linux boot process follows a defined sequence:

 The system firmware (BIOS or UEFI) performs hardware checks.
 The bootloader (GRUB) loads the Linux kernel into memory.
 The kernel initialises hardware and core subsystems.
 The init system (systemd) starts system services.
 User space becomes available for login and application execution.

Failure at any stage of this process prevents the operating system from reaching a usable state.

---

## Linux Ecosystem and Distributions

Linux refers specifically to the kernel, while the complete operating system includes GNU utilities, libraries, and system tools. Together, these components form a functional Linux-based operating system.

Linux distributions package the kernel with software management tools and configuration defaults. Ubuntu belongs to the Debian family of distributions and uses the APT package management system. Other distribution families include Red Hat-based systems using DNF and Arch-based systems using Pacman.

---

## Command-Line Foundations

Command-line tools are essential for administering headless Linux servers. Core command categories include:

File system navigation:** `ls`, `cd`, `pwd`
File operations:** `cp`, `mv`, `rm`
Process management:** `ps`, `top`, `kill`
System information:** `uname -a`, `free -h`, `df -h`

These commands allow administrators to inspect system state, manage resources, and troubleshoot issues remotely via SSH.

---

## Reflection

This week highlighted the importance of operating system architecture in determining system performance, security, and reliability. Understanding kernel design choices and the boot process provides insight into how Linux systems initialise and manage hardware resources. Familiarity with command-line tools is essential for effective server administration and prepares the groundwork for security hardening and performance evaluation in later weeks.

---

## References
Lecture slides: *System Architecture and Linux Foundations* (CMPN202 Operating Systems)

