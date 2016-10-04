---
title: "DHE keys less than 1023-bit are no longer accepted"
date: "2015-03-17T14:02:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["39"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1138554"
      title: "Bug 1138554 – NSS accepts export-length DHE keys with regular DHE cipher suites"
    - url: "https://www.mozilla.org/en-US/security/advisories/mfsa2015-70/"
      title: "MFSA 2015-70 – NSS accepts export-length DHE keys with regular DHE cipher suites"
---
In order to prevent "[Logjam](http://www.zdnet.com/article/enterprise-cloud-services-exposed-as-vulnerable-to-logjam/)" man-in-the-middle attacks, the lower length of the supported Ephemeral Diffie-Hellman (DHE) keys has been limited to 1023-bit. 512-bit export-grade cryptography is no longer available in the Mozilla products, and users may encounter the following error message on sites offering such a weak key:

**Update**: According to [Firefox Input](https://input.mozilla.org/en-US/?product=Firefox&q=ssl_error_weak_server_ephemeral_dh_key), [Firefox Support](https://support.mozilla.org/en-US/search?q=ssl_error_weak_server_ephemeral_dh_key) and other sources, a certain number of sites are known to be affected by this change. Please make sure to keep your visitors secure. If you don't know what does it mean, please notify your server administrator of the error.
