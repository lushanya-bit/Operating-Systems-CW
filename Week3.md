# Week 3 - Application Selection for Performance Testing

## Overview 
This week focuses on understanding the process management of Linux and implementing system security controls. In this week I was introduced to the exploration of process lifecycle and its states, fg and bg execution and signal handling. Remote administration was implemented through SSH key-based authentication and firewall configuration, which all contributes to secure server environment.
---

## Process States
**Commands used**
ps aux
ps -ef
top

**ps aux**
The ps aux command displays a complete list of all running processes on the ubuntu server. This output includes system and user processes, showing their process IDs (PID), ownership, CPU usage etc. In my screenshot, the results confirm that core system services are running under the root user, while the user-level processes are isolated appropriately which supports the principle of least priviledge.
