---
title: "RC4 support has been completely removed"
date: "2016-11-17T20:01:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["50", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268728"
      title: "Bug 1268728 - Remove ability to enable RC4"
---
The RC4 support has been deprecated since [Firefox 36](https://www.fxsitecompat.dev/en-CA/docs/2014/rc4-support-has-been-deprecated/) and disabled by default since [Firefox 44](https://www.fxsitecompat.dev/en-CA/docs/2015/rc4-is-now-completely-disabled-by-default/). As a temporary workaround, the users could still enable it via hidden preferences in case some intranet applications were not updated yet.

After a 1-year grace period, Firefox 50 has removed the ability to override the preferences so now the RC4 support is completely dropped. This follows Google Chrome 53 released in August which took the same security measure. From now on Firefox will just show the `SSL_ERROR_NO_CYPHER_OVERLAP` error when encountered any site using the RC4 cipher.
