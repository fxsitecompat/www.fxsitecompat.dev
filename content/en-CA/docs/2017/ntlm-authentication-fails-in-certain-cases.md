---
title: "NTLM authentication may fail against HTTPS site"
date: "2017-03-14T20:40:00-04:00"
categories: ["networking"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1346392"
      title: "Bug 1346392 - Firefox 52.0 fails to NTLM authenticate to SharePoint Server 2016 sites over TLS 1.2"
---
Firefox 52 has introduced a regression where the users cannot sign in to a site which is served via TLS 1.2 and requires an [NTLM authentication](https://en.wikipedia.org/wiki/NT_LAN_Manager). The reported application is *SharePoint Server 2016* but other sites may also be affected.

According to an investigation by Microsoft, this is due to the fact that Firefox does not downgrade the connection to HTTP/1.1 upon authentication even though NTLM is not compatible with HTTP/2.

Mozilla developers are looking for the solution. Meanwhile, users can temporarily disable HTTP/2 by flipping the hidden `network.http.spdy.enabled.http2` preference through [`about:config`](https://support.mozilla.org/kb/about-config-editor-firefox) to work around the issue.

**Update**: This issue has been fixed with Firefox 53 and Firefox ESR 52.1.
