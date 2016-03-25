---
title: "Some sites are broken when third-party cookies are blocked"
date: "2016-03-11T12:58:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1254856"
      title: "Some websites (forgeofempires.com, bet365.com, inbox.google.com) can't finish loading with \"Accept third-party cookies: Never\" checked"
aliases:
    - "/docs/2016/some-flash-sites-are-broken-when-third-party-cookies-are-blocked/"
---
Firefox 45 has introduced a regression where certain Flash sites, such as online games and live streaming videos, cannot finish loading when the browser is configured to block third-party cookies. Mozilla developers are working on the solution.

**Update**: It was discovered that the non-Flash *Google Inbox* Web application was also broken due to the same bug in the code. Corrected this article's title accordingly. The issue has been solved with Firefox 45.0.1.

**Update**: Users are reporting the *Google Inbox* issue has not been fixed with Firefox 45.0.1. There are several more sites broken when third-party cookies are blocked. We have posted [another article](https://www.fxsitecompat.com/en-CA/docs/2016/cookies-are-missing-in-xhr-post-requests-from-workers-when-third-party-cookies-are-blocked/) for that.
