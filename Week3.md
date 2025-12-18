# Week 3 - Application Selection for Performance Testing

## Overview 
This week focuses on understanding the process management of Linux and implementing system security controls. In this week I was introduced to the exploration of process lifecycle and its states, fg and bg execution and signal handling. Remote administration was implemented through SSH key-based authentication and firewall configuration, which all contributes to secure server environment.
---

## Process Management

## Process States
**Commands used**
ps aux
ps -ef
top

**Running Processes (ps aux)**
The ps aux command displays a complete list of all running processes on the ubuntu server. This output includes system and user processes, showing their process IDs (PID), ownership, CPU usage etc. In my screenshot, the results confirm that core system services are running under the root user, while the user-level processes are isolated appropriately which supports the principle of least priviledge.

**Explanation of Key Columns**
-User: Owner of process
-PID: a unique Process ID
-%CPU: CPU usage
-%MEM: Memory usage
-STAT: Current process state
-COMMAND: the command that launched the process

**Common Process States**
-R: Running
-S: Sleeping
-D: Uninterruptible sleep (I/O)
-T: Stopped (Ctrl+Z)
-Zombie: terminated

## Evidence Screenshot
![PS Aux](images/week3/ps_aux.png)

**Real-time process monitoring (top)**
top was used to observe the real time CPU and memory usage dynamically. This allowed identification of high-resource processes and sytem load trends. It provides a view that continuosly updates the running processes, CPU usage, memory consumption, process priority, runtime and the current state. In the screenshot below, it shows that most processes are owned by the root user which represents core system services. CPU utilisation is low, which indicates that the server is operating efficiently. Unlike ps aux, top is used to for live monitoring.

## Evidence Screenshot
![Top](images/week3/Top_screenshot.png)

##Process Hierarchy
**Commands Used**
pstree
pstree -p

## Bg and Fg Execution
**Commands Used**
sleep 300 &
jobs
sleep 500
bg
fg

## Process Termination
**Commands Used**
kill <PID>
killall sleep

## Process Priority
**Commands Used**
nice -n 10 sleep 400 &
top

## Explanation
-Foreground processes require user interaction
-Background processes allow multitasking
-kill sends SIGTERM gracefully
-kill -9 sends SIGKILL forcefully (unsafe if not used properly)
-nice adjusts scheduling priority to reduce CPU impact

**pstree**
This visualises the relationship between processes, and highlights how they are managed by the system.

## SSH Configuration


