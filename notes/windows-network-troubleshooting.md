# Windows Network Troubleshooting

This file documents common Windows network troubleshooting steps for IT support practice.

## Purpose

The goal of this lab is to understand how IT support technicians troubleshoot network connectivity issues from a Windows 10/11 device.

## Common Network Issues

Users may report issues such as:

* No internet connection
* Wi-Fi connected but websites will not load
* Ethernet not working
* VPN will not connect
* Cannot access a shared drive
* Cannot reach a company website or internal resource
* Slow network connection
* DNS issues
* IP address issues

## Basic Troubleshooting Process

1. Confirm whether the issue affects one user or multiple users.
2. Confirm whether the device is using Wi-Fi, Ethernet, or VPN.
3. Check if the device has an IP address.
4. Test basic connectivity.
5. Test DNS/name resolution.
6. Restart the browser or application.
7. Restart the network adapter if needed.
8. Restart the device if needed.
9. Document the issue and results.
10. Escalate if the issue affects multiple users or business-critical systems.

## Command Prompt Commands

### Check IP configuration

```cmd
ipconfig
```

### Show detailed IP configuration

```cmd
ipconfig /all
```

### Test internet connectivity by IP address

```cmd
ping 8.8.8.8
```

### Test DNS/name resolution

```cmd
ping google.com
```

### Check DNS lookup

```cmd
nslookup google.com
```

### Trace the network path

```cmd
tracert google.com
```

### Release IP address

```cmd
ipconfig /release
```

### Renew IP address

```cmd
ipconfig /renew
```

### Flush DNS cache

```cmd
ipconfig /flushdns
```

## PowerShell Commands

### Test network connection

```powershell
Test-Connection google.com
```

### View network adapter information

```powershell
Get-NetAdapter
```

### View IP configuration

```powershell
Get-NetIPConfiguration
```

## Example Scenario

### Problem

A user says their computer is connected to Wi-Fi, but websites will not load.

### Steps to Check

1. Confirm the Wi-Fi connection is active.
2. Run `ipconfig` to check IP address information.
3. Ping `8.8.8.8` to test internet connectivity.
4. Ping `google.com` to test DNS/name resolution.
5. Run `nslookup google.com` if DNS appears to be the issue.
6. Try `ipconfig /flushdns`.
7. Restart the browser.
8. Document results and escalate if needed.

## How to Think Through Results

If `ping 8.8.8.8` works but `ping google.com` fails, the issue may be related to DNS.

If both fail, the issue may be related to Wi-Fi, Ethernet, IP configuration, router, VPN, or internet access.

If only one website fails, the issue may be with that website or a specific application instead of the whole network.

## Documentation Notes

When documenting a Windows network issue, I should include:

* User or device affected
* Connection type: Wi-Fi, Ethernet, or VPN
* Error message
* IP address status
* Commands used
* Ping results
* DNS test results
* Whether one user or multiple users are affected
* Final resolution or escalation notes

## What I Am Learning

I am learning how to use Windows command-line tools to narrow down network issues. These steps help identify whether a problem is related to IP configuration, DNS, internet access, VPN, or a specific application.

## Safety Note

I should avoid uploading screenshots or command outputs that show private IP addresses, public IP addresses, usernames, computer names, company domains, or internal network information.
