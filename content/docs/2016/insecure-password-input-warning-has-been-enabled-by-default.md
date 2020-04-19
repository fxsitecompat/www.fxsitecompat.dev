---
title: "Insecure password input warning has been enabled by default"
date: "2016-12-03T14:54:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319119"
      title: "Bug 1319119 - Turn on Insecure Password Warning in Firefox Release"
aliases:
    - "/en-CA/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/"
---
Since [Firefox 46](https://www.fxsitecompat.dev/en-CA/docs/2015/non-https-sites-containing-login-form-will-be-marked-insecure/), Firefox Nightly and Developer Edition have been showing a broken padlock icon on the Address Bar when the current page has `<input type="password">` while the connection is not secure. Firefox 50 expanded this [insecure password input warning](https://twitter.com/FxSiteCompat/status/779224374742249472) to early Beta versions. Firefox 51 makes it enabled by default on all channels including the Release version.

Thought the indicator is not so prominent at this moment, there will be more warnings including [in-context UI changes](https://www.fxsitecompat.dev/en-CA/docs/2017/insecure-login-forms-now-disable-autofill-show-warning-beneath-input-control/) as part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.dev/en-CA/docs/2015/insecure-http-will-be-deprecated/). Web developers are strongly encouraged to move any sign-in form to an HTTPS page or ideally make the page itself HTTPS in order to protect customers.

This change will be made in line with Google Chrome 56 that makes a [similar change](https://blog.chromium.org/2016/09/moving-towards-more-secure-web.html) also in January 2017.
