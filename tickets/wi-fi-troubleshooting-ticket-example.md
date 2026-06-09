# Ticket Example: Wi-Fi Troubleshooting Issue

## Ticket Summary

User reports they are unable to connect to the company Wi-Fi network.

## User Impact

The user cannot access the internet, Microsoft 365 services, shared drives, VPN, or other network resources needed for daily work.

## Initial User Report

The user stated that their laptop will not connect to Wi-Fi. They reported that the issue started this morning and that websites, Outlook, and Teams will not load.

## Troubleshooting Steps

1. Confirmed when the issue started.
2. Asked whether the issue was happening in the office, at home, or remotely.
3. Asked whether other users nearby were having the same issue.
4. Confirmed Wi-Fi was enabled on the laptop.
5. Confirmed airplane mode was turned off.
6. Verified the user was attempting to connect to the correct SSID.
7. Checked Wi-Fi signal strength.
8. Forgot the saved Wi-Fi network and reconnected.
9. Restarted Wi-Fi on the laptop.
10. Restarted the computer.
11. Opened Command Prompt and checked IP configuration:

```cmd
ipconfig
```

12. Confirmed the laptop had a valid IP address, subnet mask, default gateway, and DNS server.

13. Tested connection to the default gateway:

```cmd
ping [default-gateway]
```

14. Tested internet connectivity:

```cmd
ping 8.8.8.8
```

15. Tested DNS resolution:

```cmd
nslookup google.com
```

16. Flushed the DNS cache:

```cmd
ipconfig /flushdns
```

17. Released and renewed the IP address:

```cmd
ipconfig /release
ipconfig /renew
```

18. Confirmed the user could access websites, Outlook, and Teams after reconnecting.

## Possible Causes

* Wi-Fi disabled
* Airplane mode enabled
* Incorrect Wi-Fi password
* Connected to the wrong SSID
* Weak wireless signal
* Saved Wi-Fi profile issue
* DHCP issue
* DNS issue
* Wireless adapter driver issue
* VPN issue
* Access point issue
* Network outage
* Authentication issue

## Resolution

The laptop was connected to the correct Wi-Fi network but had intermittent connectivity. The saved Wi-Fi profile was removed, the device was reconnected to the correct SSID, and the IP address was renewed. After reconnecting, the user was able to access websites, Outlook, and Teams.

## Ticket Notes

The user confirmed that Wi-Fi connectivity was restored and Microsoft 365 services were working normally.

## Escalation Criteria

This issue would be escalated to Tier 2 or the network team if:

* Multiple users were affected
* The Wi-Fi network was not visible
* The device could not receive a valid IP address
* The user could not authenticate to the wireless network
* The access point appeared to be down
* The issue affected an entire office area
* Admin permissions were required
* The issue continued after basic troubleshooting

## What I Learned

This ticket helped reinforce the importance of checking simple wireless issues first, such as Wi-Fi status, airplane mode, SSID, signal strength, and saved network profiles before moving into IP, DNS, DHCP, or access point troubleshooting.
