---
title: "Insecure login forms now disable autofill, show warning beneath input control"
date: "2017-01-19T12:25:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1217152"
      title: "Bug 1217152 - Flip prefs to disable login autofill on HTTP and enable the warning on insecure login fields"
---
As part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.com/en-CA/docs/2015/insecure-http-will-be-deprecated/), Firefox 51 has enabled the [basic warning for insecure password input](https://www.fxsitecompat.com/en-CA/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/) by default to show a broken padlock icon on the Address Bar whenever an `<input type="password">` is found on a non-HTTPS page. Firefox 52 advances this security measure by disabling autofill on such insecure login forms and rather showing a more prominent [contextual warning message](https://developer.mozilla.org/en-US/docs/Web/Security/Insecure_passwords) just below the `<input>` element.

Webmasters are strongly encouraged to move any form to an HTTPS page to let customers sign in safely and securely. In case you don't know, [Let's Encrypt](https://letsencrypt.org/) gives you a trusted SSL/TLS certificate for free.
