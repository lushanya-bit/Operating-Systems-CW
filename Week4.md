# Week 4 - Initial System Configuration & Security Implementation

## Overview
In this week we aimed to implement advanced security. It introduced MAC, intrusion detection etc. These collectively strengthened the sytem against priviledge misuse while monitoring the security.

## Mandatory Access Control (MAC)
Ubuntu Server uses AppArmor as its mandatory access control security base. It enforces security policies on applications by restricting the resources they are allowed to access.

The active MAC system was verfied using:

![AA Status](images/week4/aa_status.png)

This command confirms that AppArmor was active.

Two operational modes were observed:
- **Enforce mode** - Policy violations are blocked and logged.
- **Complain mode** - Violations are logged but not blocked.

## AppArmor Status Reporting Script

![AA Script](images/week4/aa_script1.png)
![AA Script2](images/week4/aa_script2.png)

This script was created to summarise AppArmor status. The script confirms that AppArmor is installed, counts the loaded profiles, seperates enforced and complain modes and also produces a report like shown below.

![AA Report](images/week4/aa_report.png)

### MAC VS DAC
-**DAC** relies on user ownership and permissions.
-**MAC** enforces centrally defined security policies that cannot be override by users.

## Intrusion Detection with fail2ban
