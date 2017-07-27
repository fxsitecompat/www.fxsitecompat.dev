---
title: "Web Console now warns sites using SSLv3 and RC4"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1092835"
      title: "Bug 1092835 – Log usage of weak ciphers in the console"
---
The [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) will display warnings on sites using the SSL 3.0 protocol or the RC4 cipher suites, since those are deprecated and insecure. Webmasters are strongly recommended to update their servers to offer stronger encryption.

**Update**: The SSLv3 support has been [removed with Firefox 39](https://www.fxsitecompat.com/en-CA/docs/2015/sslv3-support-has-been-removed/).
