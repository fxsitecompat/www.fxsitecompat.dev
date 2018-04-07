---
title: "Basic auth credentials are now encoded in UTF-8 instead of ISO-8859-1"
date: "2018-04-06T22:35:00-04:00"
categories: ["networking"]
tags: []
versions: ["59"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1419658"
      title: "Bug 1419658 - Change Basic authentication request header username and password character encoding to UTF-8 (used to be ISO-8859-1)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449112"
      title: "Bug 1449112 - JBoss authentication issue since FF 59 (problem with accents in authentication window ?) "
---
Previously, Firefox was using the ISO-8859-1 character encoding for the username and password in Basic HTTP authentication requests. Firefox 59 and later will use UTF-8 instead for the `Authorization` header to make sure non-ASCII characters like French accented letters are encoded properly.

If your site only allows alphanumeric and common symbols in user credentials, this change won't be a problem. However, sites accepting non-ASCII usernames and/or passwords have to be updated to support both ISO-8859-1 and UTF-8, or users may have difficulty in signing in.

Since Google Chrome is already using UTF-8, popular application frameworks are apparently sniffing the `User-Agent` header to determine which character encoding to expect from the browser, as noted in [RFC 7617](https://tools.ietf.org/html/rfc7617#appendix-B.3). The same interoperability approach may apply to Firefox 59 and later. Given that Firefox 52 [Extended Support Release](https://www.mozilla.org/en-US/firefox/organizations/) (ESR) will be available until August 2018, sniffing code should check not only the browser name but also the version number.

So far *JBoss Enterprise Application Platform (EAP)* is known to be affected by this change.
