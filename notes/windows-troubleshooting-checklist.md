# Windows 10/11 Troubleshooting Checklist

This file documents a basic Windows 10/11 troubleshooting process for IT support practice.

## Purpose

The goal of this checklist is to practice a clear troubleshooting workflow for common Windows desktop support issues. This is useful for help desk, desktop support, and IT support roles.

## Basic Troubleshooting Process

1. Identify the issue
2. Ask what changed recently
3. Check the basics first
4. Reproduce the problem if possible
5. Check system settings and error messages
6. Use built-in Windows tools
7. Try one fix at a time
8. Document the steps taken
9. Confirm the issue is resolved
10. Escalate if needed

## Common Issues to Check

* Computer running slowly
* Application not opening
* Internet or Wi-Fi not working
* Printer not responding
* User cannot sign in
* Password or account access issue
* Windows updates failing
* External monitor not displaying
* Audio or microphone not working
* File or folder access issue

## Windows Tools to Use

### Task Manager

Used to check running applications, system performance, startup apps, and processes.

### Device Manager

Used to check hardware devices, drivers, disabled devices, and device errors.

### Event Viewer

Used to review Windows logs and error messages.

### Windows Update

Used to check for missing updates, failed updates, and restart requirements.

### Settings App

Used to check network, display, sound, accounts, apps, and system settings.

### Control Panel

Used for some classic Windows settings and troubleshooting areas.

## Command-Line Tools

Useful Windows commands include:

```cmd
ipconfig
ping
tracert
nslookup
sfc /scannow
chkdsk
gpupdate /force
```

## Example Troubleshooting Scenario

### Problem

A user reports that their computer is connected to Wi-Fi but cannot access websites.

### Steps to Check

1. Confirm Wi-Fi is connected
2. Check if other websites work
3. Check IP address with `ipconfig`
4. Test connection with `ping 8.8.8.8`
5. Test DNS with `ping google.com`
6. Restart the browser
7. Restart the network adapter if needed
8. Document results

## IT Support Notes

When documenting a Windows issue, I should include:

* User or device affected
* Problem description
* Error messages
* Troubleshooting steps taken
* Tools or commands used
* Resolution or escalation notes
* Final status

## What I Am Learning

I am learning how to approach Windows troubleshooting in an organized way. This helps me build better support habits, document clearly, and think through common IT problems step by step.
