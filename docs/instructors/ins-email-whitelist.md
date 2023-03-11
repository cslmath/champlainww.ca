---
title: Whitelist the email server
authors:
    - Malcolm Harper
date: 2023-03-11
tags:
    - instructors
    - email
    - configuration
    - spam
---

# WeBWorK Emails and Spam

Anti-spam and, in particular, anti-phishing measures are becoming more and more stringent both globally and at the college.
Since WeBWorK, by its nature, sends email to instructors _on behalf of_ students, WeBWorK emails risk getting caught in various spam filters.

To avoid, as much as possible, the classification of WeBWorK server emails as spam by the Office 365 email system at the college, I suggest three things:

1. Whitelist our email server in Office 365.
1. Check your _Junk_ email folder regularly for false positives.
1. Train Office 365 that any false positives are not spam.

## Whitelist the WeBWorK email server

Add `mg.champlainww.ca` as a _safe domain_ in your Office 365 Junk email settings.

1. Go to the _Junk email_ settings on the Office 365 website.
    - You can either go directly to
    [`outlook.office.com/mail/options/mail/junkEmail`](https://outlook.office.com/mail/options/mail/junkEmail)
    logging in if necessary,
    - or from the usual mail view:
        * Click the three dots (More options),
        * Choose _Rules_ :material-arrow-right: _Manage rules_,
        * Then select _Junk email_ from the _Mail_ menu.
1. _Add_ a new entry under _Safe senders and domains_ with the contents `mg.champlainww.ca`
    - Click _Add_, type `mg.champlainww.ca`, then enter :material-keyboard-return:
1. (Optional) Add a second new entry with the contents `champlainww.ca`
1. Scroll down to _Save_ your changes

## Check your junk email directory regularly

I suggest that you check your Office 365 Junk email folder at least once a week (more often is better).
Even if you use another email client, if the problem is that Office 365 is labelling WeBWorK email as spam,
then we have to train Office 365 otherwise.

Check the _Junk Email_ folder in your account.
If there is email there that shouldn't be, tag it as ham (not spam).
There are a few ways to do this:

- Right-click the email and _Report_ :material-arrow-right: _Not junk_
- or click _It's not junk_ at the top of the email when it is displayed,
- or use the _Report_ drop-down in the menu bar.
