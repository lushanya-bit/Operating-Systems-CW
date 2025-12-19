#Week 1 - System Planning and distribution selection

## Overview
This week focuses on planning the environments that will be used and selecting suitable Linux distributions for both the server and the workstation systems. The aim of this task was to design a secure client-server setup, which will support future configuration tasks.
---
## System Architecture Diagram

+----------------------------------+
|          Host Machine            |
|          (Windows OS)            |
|                                  |
|        PowerShell (SSH Client)   |
+-----------------+----------------+
                  |
                  |SSH
                  |
+-----------------V----------------+
|        Ubuntu Server VM          |
|      (24.04.43 LTS, Headless)    |
|                                  |
|      Firewall: SSH only          |
+----------------------------------+
                  |
                Virtual Box

This system architecture follows a client-server model. The Ubuntu Server runs as a headless virtual machine hosted in VirtualBox. The host machine running Windows acts as  the workstation, using PowerShell as a SSH client to administer the server. Firewall rules on the server restricts access to SSH only which improves security.

## Server Distribution  
**Chosen Distribution:** Ubuntu Server 24.04.03 LTS

**Justification**
-Long Term support (LTS) provides stability and security updates
-Suitable for headless server operations
-Used widely in the industry and cloud environments
-Strong community support
-Popular for desktops

**Alternatives Considered**
-Fedora Linux (provides excellent hardware support but requires frequent upgrades)
-Linux Mint (focuses on user privacy but has poor support for new hardware)

Ubuntu Server was selected due to its excellent stability, usability and it is lightweight. It's extensive documentation makes it suitable for headless server environments and learning based deployments.

## Workstation Configuration

**Chosen Option:** Host Machine with SSH Client (PowerShell)

**Justification**
The workstation used is the host Windows PowerShell. PowerShell has a built-in SSH client, which allows secure access to the Linux server without requiring a seperate virtual machine. This reduces the usage of resources while still supporting all administrative tasks.

PowerShell was chosen due to the built-in SSH support and its reliability.

## Network Configuration Plan
-Virtual machines configured to commmunicate via a virual network
-Server firewall configured to allow SSH traffic only
-SSH used as the main server access method
-Network configuration documented to provide consistency and security

## CLI System Specification Evidence
The commands below were executed on the server to verify system specifications

## Commands Demonstrated
-`uname -a`
-`free -h`
-`df -h`
-`ip addr`

##Evidence
![Week 1 CLI Evidence](images/week1/Screenshot_2025-12-10_155001.png)
---

##Reflection
After completing this week, a strong foundation was established . Planning the system architecture and selecting the appropriate distributions helped to ensure that the environment is not only strong but also manageable.


