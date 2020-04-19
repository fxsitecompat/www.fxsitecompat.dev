---
title: "Firefox 57 introduces new CSS engine, changes some behaviours"
date: "2017-09-27T03:42:00-04:00"
categories: ["css"]
tags: []
releases: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1365771"
      title: "Bug 1365771 - stylo: Tracking bug for behavior changes in stylo"
---
Firefox 57 shipping in November 2017 comes with a [new CSS engine](https://blog.mozilla.org/blog/2017/09/26/firefox-quantum-beta-developer-edition/) called Quantum CSS or Stylo. This is exciting news for both end users and web developers, because rendering of web pages will be faster than ever before. However, since Stylo has been completely reinvented, there are dozens of behaviour differences from the legacy CSS engine powered Firefox 56 and prior.

Please refer to the [developer release notes on MDN](https://developer.mozilla.org/Firefox/Releases/57#Quantum_CSS_notes) for those known changes. We'll cover regressions found after the final release of Firefox 57. In the meantime, developers are encouraged to test their sites and apps using [Developer Edition](https://www.mozilla.org/firefox/developer/) and [let us know any problems](https://www.fxsitecompat.dev/en-CA/contribute/) you may have encountered.
