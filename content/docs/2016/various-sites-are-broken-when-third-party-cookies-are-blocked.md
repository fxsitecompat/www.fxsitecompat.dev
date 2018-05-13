---
title: "Various sites are broken when third-party cookies are blocked"
date: "2016-03-11T12:58:00-05:00"
categories: ["dom", "plugins", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1254856"
      title: "Bug 1254856 - Some websites (forgeofempires.com, bet365.com, inbox.google.com) can't finish loading with \"Accept third-party cookies: Never\" checked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257861"
      title: "Bug 1257861 - Firefox 45 fails to send Cookie header with XHR post requests done from a web worker when third-party cookies are blocked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257236"
      title: "Bug 1257236 - The \"inbox.google.com\" page keeps refreshing on and on with \"Accept third-party cookies: Never\" checked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249083"
      title: "Bug 1249083 - Google Sheets not evaluating cells"
aliases:
    - "/en-CA/docs/2016/some-flash-sites-are-broken-when-third-party-cookies-are-blocked/"
    - "/en-CA/docs/2016/some-sites-are-broken-when-third-party-cookies-are-blocked/"
    - "/en-CA/docs/2016/cookies-are-missing-in-xhr-post-requests-from-workers-when-third-party-cookies-are-blocked/"
---
Firefox 45 has introduced a regression where certain Flash sites, such as online games and live streaming videos, cannot finish loading when the browser is configured to block third-party cookies. Mozilla developers are working on the solution.

**Update**: It was discovered that the non-Flash *Google Inbox* Web application was also broken due to the same bug in the code. Corrected this article's title accordingly. The issue has been solved with Firefox 45.0.1.

**Update**: Users are reporting the *Google Inbox* issue has not been fixed with Firefox 45.0.1. *Google Sheets* and several more sites have also been found broken when third-party cookies are blocked. We have discovered in one of these bugs that [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) POST requests made in [workers](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers) do not send the HTTP `Cookie` header even if those resources are on the [same origin](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy). Mozilla developers are investigating the details.

**Update**: This bug has been fixed with Firefox 45.0.2.
