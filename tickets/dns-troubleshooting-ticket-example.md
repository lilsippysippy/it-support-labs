# Ticket Example: DNS Troubleshooting Issue

## Ticket Summary

User reports they are connected to the network but cannot access websites by name.

## User Impact

The user cannot access websites, Microsoft 365 services, or other cloud-based resources needed for daily work.

## Initial User Report

The user stated that their computer shows it is connected to the network, but websites will not load. They reported that Outlook and Teams were also having connection issues.

## Troubleshooting Steps

1. Confirmed when the issue started.
2. Asked whether the issue affected one website or multiple websites.
3. Asked whether other users in the same area were having the same issue.
4. Verified the computer was connected to the network.
5. Opened Command Prompt and checked IP configuration:

```cmd
ipconfig
```

6. Confirmed the computer had a valid IP address, subnet mask, default gateway, and DNS server.

7. Tested basic internet connectivity by pinging a public IP address:

```cmd
ping 8.8.8.8
```

8. Tested DNS resolution:

```cmd
nslookup google.com
```

9. Tested connectivity by domain name:

```cmd
ping google.com
```

10. Flushed the DNS cache:

```cmd
ipconfig /flushdns
```

11. Released and renewed the IP address:

```cmd
ipconfig /release
ipconfig /renew
```

12. Tested website access again.
13. Confirmed Microsoft 365 services loaded after troubleshooting.
14. Documented all steps and results in the ticket.

## Possible Causes

* DNS server issue
* Stale DNS cache
* Incorrect DNS settings
* DHCP configuration issue
* VPN DNS issue
* Browser cache issue
* Network outage
* ISP issue
* Internal DNS record issue

## Resolution

The workstation had network connectivity, but DNS resolution was failing. The DNS cache was flushed, and the IP address was released and renewed. After renewal, DNS resolution worked successfully and the user was able to access websites and Microsoft 365 services.

## Ticket Notes

The user confirmed that websites, Outlook, and Teams were working normally after troubleshooting.

## Escalation Criteria

This issue would be escalated to Tier 2 or the network team if:

* Multiple users were affected
* The DNS server could not be reached
* Internal company resources would not resolve
* DHCP continued assigning incorrect DNS information
* VPN DNS settings were not working
* The issue returned after troubleshooting
* Admin permissions were required

## What I Learned

This ticket helped reinforce the difference between general network connectivity and DNS resolution. A device may be connected to the network and still fail to access websites if DNS is not working correctly.
