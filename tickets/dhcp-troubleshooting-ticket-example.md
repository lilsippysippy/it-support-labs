# Ticket Example: DHCP Troubleshooting Issue

## Ticket Summary

User reports they cannot connect to the network from their Windows computer.

## User Impact

The user cannot access the internet, Microsoft 365 services, shared drives, or other network resources needed for daily work.

## Initial User Report

The user stated that their computer shows a network connection issue and they are unable to access websites, email, or Teams.

## Troubleshooting Steps

1. Confirmed when the issue started.
2. Asked whether the user was connected by Ethernet or Wi-Fi.
3. Asked whether other users nearby were having the same issue.
4. Checked the physical connection.
5. Verified the Ethernet cable was securely connected.
6. Checked for link lights on the network port.
7. Opened Command Prompt and ran:

```cmd
ipconfig
```

8. Found that the workstation had an APIPA address beginning with `169.254`.

9. Ran the following commands:

```cmd
ipconfig /release
ipconfig /renew
```

10. Checked the updated IP configuration:

```cmd
ipconfig /all
```

11. Confirmed the workstation received a valid IP address, subnet mask, default gateway, and DNS server.

12. Tested the default gateway:

```cmd
ping [default-gateway]
```

13. Tested internet connectivity:

```cmd
ping 8.8.8.8
```

14. Tested DNS resolution:

```cmd
nslookup google.com
```

15. Confirmed the user could access websites and Microsoft 365 services.

## Possible Causes

* DHCP server unavailable
* DHCP lease issue
* Bad Ethernet cable
* Bad wall port
* Switch port issue
* Incorrect VLAN
* Wi-Fi issue
* Network adapter issue
* DHCP scope exhausted
* Static IP conflict

## Resolution

The workstation had an APIPA address, which indicated it did not receive a valid IP address from DHCP. After releasing and renewing the IP address, the workstation received valid network settings and connectivity was restored.

## Ticket Notes

The user confirmed they were able to access websites, Outlook, Teams, and shared resources after troubleshooting.

## Escalation Criteria

This issue would be escalated to Tier 2 or the network team if:

* The workstation continued receiving a `169.254.x.x` address
* Multiple users were affected
* The DHCP server was unreachable
* The DHCP scope appeared exhausted
* A switch port or VLAN issue was suspected
* The device could not reach the default gateway
* Admin permissions were required
* The issue returned after troubleshooting

## What I Learned

This ticket helped reinforce how DHCP provides network settings to a device. If a Windows computer receives a `169.254.x.x` address, it usually means the device could not get an IP address from DHCP.
