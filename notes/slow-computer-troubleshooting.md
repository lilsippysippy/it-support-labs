# Slow Computer Troubleshooting

## Overview

This note documents a basic troubleshooting process for a Windows computer that is running slowly. Slow performance is a common help desk issue and can be caused by software, hardware, startup programs, low disk space, malware, updates, or resource usage.

## Common User Report

A user may report:

* “My computer is running slow.”
* “It takes forever to start up.”
* “Programs keep freezing.”
* “Everything is lagging.”
* “My computer was fine yesterday, but now it is slow.”

## Initial Questions to Ask

Before troubleshooting, ask the user:

1. When did the issue start?
2. Is the whole computer slow or only one application?
3. Did anything recently change, such as updates, new software, or hardware?
4. Does the issue happen after rebooting?
5. Are other users or devices having the same issue?
6. Is the computer on Wi-Fi, Ethernet, or VPN?
7. Are there any error messages?

## Troubleshooting Steps

### 1. Restart the Computer

Restart the computer to clear temporary issues, stuck processes, or pending updates.

### 2. Check Task Manager

Open Task Manager and check:

* CPU usage
* Memory usage
* Disk usage
* Network usage
* Startup apps
* Unresponsive processes

High CPU, memory, or disk usage can help identify what is slowing the system down.

### 3. Check Startup Apps

Disable unnecessary startup apps if allowed by company policy.

Too many startup apps can make the computer slow during login and startup.

### 4. Check Disk Space

Verify that the computer has enough free storage space.

Low disk space can cause slow performance, update issues, and application problems.

### 5. Check Windows Updates

Check for pending Windows updates or failed updates.

A computer may run slowly during updates or after failed update attempts.

### 6. Check for Malware or Suspicious Activity

Run an approved antivirus or endpoint security scan if malware is suspected.

Warning signs may include:

* Pop-ups
* Unknown programs
* Browser redirects
* Unusual startup items
* High resource usage from unknown processes

### 7. Check Device Manager

Open Device Manager and look for warning icons.

Driver issues can cause system instability or poor performance.

### 8. Review Event Viewer

Check Event Viewer for repeated errors, warnings, crashes, or disk-related issues.

### 9. Test Network Performance

If the issue only happens with websites, email, cloud apps, or shared drives, test network connectivity.

Useful commands include:

```cmd
ping 8.8.8.8
ipconfig
nslookup google.com
tracert google.com
```

### 10. Document Findings

Document what was checked, what was found, and what action was taken.

## Possible Causes

* Too many startup programs
* High CPU usage
* High memory usage
* High disk usage
* Low storage space
* Pending or failed Windows updates
* Malware or unwanted software
* Outdated drivers
* Failing hard drive
* Network or VPN issue
* Application-specific issue
* Old hardware

## Possible Resolutions

* Restart the computer
* Close unnecessary applications
* Disable unnecessary startup apps
* Free up disk space
* Install updates
* Restart stuck services
* Remove unwanted software if approved
* Run malware scan
* Update drivers
* Escalate for hardware diagnostics if needed

## Escalation Criteria

Escalate the issue if:

* The computer has signs of hardware failure
* The hard drive may be failing
* Malware is suspected and cannot be removed
* The user cannot work after basic troubleshooting
* Admin rights are required
* The issue affects multiple users
* The computer repeatedly crashes or shows blue screen errors

## Example Ticket Note

User reported that their Windows computer was running slowly and applications were freezing. Checked Task Manager and found high disk usage. Restarted the computer, checked startup apps, verified disk space, and confirmed Windows updates were pending. After updates completed and the system restarted, performance improved. User confirmed the computer was working normally.

## What I Learned

Slow computer issues require checking both simple and technical causes. Starting with user questions, Task Manager, disk space, startup apps, updates, and basic system checks can help narrow down the problem before escalating.
