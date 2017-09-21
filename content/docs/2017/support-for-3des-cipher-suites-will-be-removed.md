---
title: "Support for 3DES cipher suites will be removed"
date: "2017-09-20T20:40:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227524"
      title: "Bug 1227524 - Establish deprecation date for 3DES"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386754"
      title: "Bug 1386754 - Disable 3DES in TLS Handshake for Nightly builds"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386908"
      title: "Bug 1386908 - Disable 3DES in TLS Handshake for early beta builds"
---
Firefox has deprecated the [Triple DES](https://en.wikipedia.org/wiki/Triple_DES) (3DES) cipher suites in TLS handshake, and will remove the support in the near future. It has already been disabled on the Firefox Nightly channel starting with version 57, showing the `SSL_ERROR_NO_CYPHER_OVERLAP` error upon access to affected sites.

The next step is to disable it on the early Beta channel including Developer Edition, but various sites including *Wall Street Journal* and *Mibbit* are known to be still using the weak cipher. Webmasters running an HTTPS site are encouraged to review the server configuration using [Observatory by Mozilla](https://observatory.mozilla.org/).
