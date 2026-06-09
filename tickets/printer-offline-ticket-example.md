# Ticket Example: Printer Offline Issue

## Ticket Summary

User reports they are unable to print because the printer shows as offline.

## User Impact

The user cannot print documents needed for daily work.

## Initial User Report

The user stated that they sent several documents to the printer, but nothing printed. The printer status on their computer shows as offline.

## Troubleshooting Steps

1. Confirmed the printer name and location with the user.
2. Asked whether other users were able to print to the same printer.
3. Checked whether the printer was powered on.
4. Verified that the printer had paper and toner.
5. Checked the printer display for errors, paper jams, or warning messages.
6. Confirmed the printer was connected to the network.
7. Asked the user to restart the printer.
8. Checked the print queue for stuck jobs.
9. Cleared stuck print jobs if needed.
10. Restarted the Print Spooler service.
11. Verified that the correct printer was selected as the default printer.
12. Checked whether the printer was set to “Use Printer Offline.”
13. Sent a test page to confirm printing worked.

## Possible Causes

* Printer powered off
* Network connection issue
* Paper jam
* Low toner or paper
* Stuck print job
* Print Spooler service issue
* Incorrect default printer
* Printer set to offline mode
* Printer driver issue

## Resolution

The printer had a stuck print job in the queue. The print queue was cleared, the Print Spooler service was restarted, and the user was able to print successfully.

## Ticket Notes

The user confirmed that the test page printed successfully and that normal printing was restored.

## Escalation Criteria

This issue would be escalated to Tier 2, desktop support, or the printer vendor if:

* The printer remained offline after restarting
* Multiple users could not print
* The printer had a hardware error
* The printer could not connect to the network
* The driver needed to be reinstalled with admin permissions
* The printer required vendor maintenance

## What I Learned

This ticket helped reinforce the importance of checking simple causes first, such as power, paper, toner, print queue status, and printer connectivity before escalating the issue.
