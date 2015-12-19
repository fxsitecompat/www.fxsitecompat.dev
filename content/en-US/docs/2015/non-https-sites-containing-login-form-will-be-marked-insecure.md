---
title: "Non-HTTPS sites containing login form will be marked insecure"
date: "2015-10-21T14:38:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["45"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1188121": "Bug 1188121 - [userstory] CC: Warning for password on non-secure connection"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1179961": "Bug 1179961 - Use a lock with a strikethrough for HTTP pages that have Password Fields in the Control Center"
---
Firefox now shows a [broken padlock icon](https://bug1179961.bmoattachments.org/attachment.cgi?id=8662392) on the location bar when the current page has `<input type="password">` and the connection is not secure. Not only the page the password will be sent but also the page the login form presents must use the HTTPS protocol to [protect user credentials from remote attackers](https://developer.mozilla.org/en-US/docs/Web/Security/Insecure_passwords).

No budget for a TLS certificate? Don't worry. From November 2015, [Let's Encrypt](https://letsencrypt.org/), a new certificate authority run by Mozilla and others, gives you a trusted certificate for free.

**Update**: This functionality has been disabled on Developer Edition due to a couple of blocker bugs, but will be [enabled soon](https://bugzilla.mozilla.org/show_bug.cgi?id=1221206).
