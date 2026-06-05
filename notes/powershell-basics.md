# PowerShell Basics

This file documents beginner PowerShell commands used for Windows IT support practice.

## Purpose

The goal of this lab is to practice basic PowerShell commands that can help with Windows troubleshooting, system information, processes, services, and support documentation.

## Why PowerShell Matters

PowerShell is useful in IT support because it can help technicians gather system information, check services, manage files, troubleshoot devices, and automate repeated tasks.

## Basic PowerShell Commands

### Show current location

```powershell
Get-Location
```

### List files and folders

```powershell
Get-ChildItem
```

### Change directories

```powershell
Set-Location Documents
```

### Clear the screen

```powershell
Clear-Host
```

## System Information

### Show computer information

```powershell
Get-ComputerInfo
```

### Show current user

```powershell
whoami
```

### Show Windows version information

```powershell
winver
```

## Process Commands

### List running processes

```powershell
Get-Process
```

### Find a specific process

```powershell
Get-Process -Name notepad
```

### Stop a process

```powershell
Stop-Process -Name notepad
```

## Service Commands

### List services

```powershell
Get-Service
```

### Check a specific service

```powershell
Get-Service -Name Spooler
```

### Restart the print spooler service

```powershell
Restart-Service -Name Spooler
```

## Network Commands

### Test connectivity

```powershell
Test-Connection google.com
```

### View IP configuration

```powershell
Get-NetIPConfiguration
```

### View network adapters

```powershell
Get-NetAdapter
```

## Practice Lab

Commands practiced:

```powershell
Get-Location
Get-ChildItem
Set-Location Documents
Clear-Host
Get-ComputerInfo
whoami
Get-Process
Get-Service
Get-Service -Name Spooler
Test-Connection google.com
Get-NetIPConfiguration
Get-NetAdapter
```

## Example Troubleshooting Scenario

### Problem

A user reports that their printer is not printing.

### Steps to Check

1. Confirm the printer is powered on and connected.
2. Check whether other users are affected.
3. Check the print queue.
4. Check the Print Spooler service.
5. Restart the Print Spooler if needed.
6. Document the results.

### PowerShell Command

```powershell
Restart-Service -Name Spooler
```

## What I Am Learning

I am learning how PowerShell can be used to gather information, check services, test connectivity, and support Windows troubleshooting. These skills are useful for help desk, desktop support, and IT support roles.

## IT Support Notes

When using PowerShell, I should document:

* The command used
* The result or error message
* Whether I ran it as administrator
* Any changes made
* Whether the issue was resolved or escalated

## Safety Note

I should be careful with PowerShell commands that change settings, stop services, remove files, or affect user accounts. In a real work environment, changes should follow proper approval and documentation procedures.
