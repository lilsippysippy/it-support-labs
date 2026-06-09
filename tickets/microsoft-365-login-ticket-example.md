# Ticket Example: Microsoft 365 Login Issue

## Ticket Summary

User reports they are unable to sign in to Microsoft 365.

## User Impact

The user cannot access Outlook, Teams, OneDrive, SharePoint, or other Microsoft 365 services needed for daily work.

## Initial User Report

The user stated that they are receiving an error when trying to sign in to Microsoft 365. They are unable to access their email and Teams messages.

## Troubleshooting Steps

1. Confirmed the user’s name, username, and affected Microsoft 365 services.
2. Asked the user when the issue started and whether they recently changed their password.
3. Confirmed whether the issue was happening in the browser, desktop apps, mobile apps, or all locations.
4. Asked the user to try signing in through a web browser.
5. Verified that the user was entering the correct username format.
6. Checked whether Caps Lock was enabled.
7. Asked the user if they received any MFA prompts.
8. Confirmed whether the user had access to their MFA method, such as phone, authenticator app, or email.
9. Checked for possible account lockout.
10. Reset the user’s password if approved by policy.
11. Had the user attempt to sign in again with the temporary password.
12. Confirmed the user could complete MFA successfully.
13. Asked the user to restart Outlook and Teams.
14. Verified that the user could access Outlook, Teams, and OneDrive after login.

## Possible Causes

* Incorrect password
* Expired password
* Account lockout
* MFA issue
* Incorrect username format
* Cached credentials
* Browser issue
* Microsoft 365 service issue
* Conditional access or permission issue

## Resolution

The user’s account was locked after multiple failed sign-in attempts. The account was unlocked, the password was reset according to policy, and the user was able to sign in successfully after completing MFA.

## Ticket Notes

The user confirmed access to Outlook, Teams, and OneDrive after the password reset and account unlock. No further issues were reported.

## Escalation Criteria

This issue would be escalated to Tier 2, identity management, or the Microsoft 365 administrator if:

* The account could not be unlocked
* MFA methods were missing or unavailable
* The user could not receive MFA prompts
* The user’s license was missing
* Multiple users were affected
* There were signs of a possible compromised account
* Conditional access policies blocked the sign-in

## Security Notes

Password resets and MFA changes should always follow company identity verification procedures. A technician should never ask for or store a user’s password or MFA code.

## What I Learned

This ticket helped reinforce the importance of verifying the user’s identity, checking account status, understanding MFA issues, and documenting each step clearly during Microsoft 365 login troubleshooting.
