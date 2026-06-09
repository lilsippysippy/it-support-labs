# DHCP Troubleshooting

## Overview

This note documents basic DHCP troubleshooting steps for Windows support and help desk environments. DHCP stands for Dynamic Host Configuration Protocol. It automatically assigns network settings to devices, including IP address, subnet mask, default gateway, and DNS servers.

DHCP issues can cause users to lose network access or receive an invalid IP address.

## Common User Report

A user may report:

* “I cannot connect to the internet.”
* “My computer says unidentified network.”
* “I am connected, but nothing loads.”
* “I cannot access shared drives.”
* “My computer worked yesterday, but now it has no connection.”

## What DHCP Does

DHCP automatically gives a device the network information it needs to communicate.

This usually includes:

* IP address
* Subnet mask
* Default gateway
* DNS server addresses

Without DHCP, a device may not receive valid network settings.

## APIPA Address

If a Windows computer cannot contact a DHCP server, it may assign itself an APIPA address.

APIPA addresses usually start with:

```text
169.254.x.x
```

If a computer has a 169.254 address, that usually means it did not receive an IP address from DHCP.

## Basic DHCP Troubleshooting Steps

### 1. Confirm the Issue

Ask the user when the issue started and whether other users nearby are affected.

### 2. Check Physical Connection

If using Ethernet, check:

* Cable is connected
* Cable is not damaged
* Link lights are active
* Wall port is working

If using Wi-Fi, check:

* Connected to the correct wireless network
* Wi-Fi is enabled
* Signal strength is acceptable

### 3. Check IP Configuration

Open Command Prompt and run:

```cmd
ipconfig
```

Look for:

* IP address
* Subnet mask
* Default gateway
* DNS server

### 4. Check for APIPA

If the IP address starts with `169.254`, the device likely did not receive an address from DHCP.

### 5. Release and Renew the IP Address

Run:

```cmd
ipconfig /release
ipconfig /renew
```

This asks the DHCP server for a new IP address.

### 6. Check Full Network Configuration

Run:

```cmd
ipconfig /all
```

This shows detailed network information, including DHCP status and DNS servers.

### 7. Test the Default Gateway

Ping the default gateway:

```cmd
ping [default-gateway]
```

If the device cannot reach the gateway, there may be a local network, cable, Wi-Fi, VLAN, or switch issue.

### 8. Restart the Network Adapter

Disable and re-enable the network adapter if needed.

### 9. Restart the Computer

Restarting can clear temporary network problems.

### 10. Check Whether Other Users Are Affected

If multiple users are affected, the issue may be with:

* DHCP server
* Switch
* VLAN
* Wireless access point
* Router
* Network outage

## Useful Commands

```cmd
ipconfig
ipconfig /all
ipconfig /release
ipconfig /renew
ping [default-gateway]
ping 8.8.8.8
nslookup google.com
```

## Possible Causes

* DHCP server unavailable
* Bad Ethernet cable
* Bad wall port
* Switch port issue
* Incorrect VLAN
* Wi-Fi issue
* Network adapter issue
* DHCP scope exhausted
* Static IP conflict
* Incorrect network configuration

## Escalation Criteria

Escalate the issue if:

* Multiple users are affected
* The device keeps receiving a 169.254 address
* DHCP is not assigning addresses
* The DHCP scope may be exhausted
* A switch port or VLAN issue is suspected
* The device cannot reach the default gateway
* Admin permissions are required
* Network infrastructure needs to be checked

## Example Ticket Note

User reported they could not connect to the network. Checked IP configuration and found the workstation had a 169.254 address. Verified Ethernet cable was connected and link lights were active. Ran `ipconfig /release` and `ipconfig /renew`. The workstation received a valid IP address from DHCP and network connectivity was restored. User confirmed access to internet and Microsoft 365 services.

## What I Learned

DHCP issues can prevent a device from receiving valid network settings. Checking the IP address, looking for APIPA, and using release/renew commands can help identify whether the issue is related to DHCP, physical connectivity, or network infrastructure.
