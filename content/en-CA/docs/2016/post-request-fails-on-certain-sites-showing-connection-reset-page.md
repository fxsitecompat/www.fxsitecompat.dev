---
title: "POST request fails on certain sites, showing connection reset page"
date: "2016-05-20T19:14:00-04:00"
categories: ["networking"]
tags: []
versions: ["46"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269055"
      title: "Bug 1269055 - RFE - auto retry failed POST"
---
Firefox 46 has changed the way to handle broken connections so that it will no longer automatically retry unsafe requests such as POST. However, various Web sites do not work with the new behaviour, resulting in an error page "connection to the server was reset", because they expect the browser to retry connections even for POST requests. *KanColle*, a popular Japanese Flash game is known to be affected.

Although this issue is rarely triggered, Firefox 47 has reverted a part of the original change for the maximum interoperability, will retry broken connections as before if it is reused.

Webmasters can work around the issue by deferring the server's persistent connection timeout. Given that Firefox uses 115 seconds for HTTP/1.x and 180 seconds for HTTP/2, server-side recommendations will be longer than 120 seconds and 185 seconds respectively.
