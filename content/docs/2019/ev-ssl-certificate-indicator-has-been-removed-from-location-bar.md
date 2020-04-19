---
title: "EV SSL certificate indicator has been removed from location bar"
date: "2019-09-04T22:40:00-04:00"
categories: ["privacy-security"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1572936"
      title: "Bug 1572936 - Move EV cert UI out of URL Bar"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o18n0SZRyUE/discussion"
      title: "Intent to Ship: Move Extended Validation Information out of the URL bar"
    - url: "https://blog.mozilla.org/security/2019/10/15/improved-security-and-privacy-indicators-in-firefox-70/"
      title: "Mozilla Security Blog: Improved Security and Privacy Indicators in Firefox 70"
---
While this is not a site compatibility issue but rather a user experience matter, it might be worth mentioning that the Extended Validation (EV) SSL certificate indicator is no longer displayed in the location bar on Firefox 70 and later due to the doubts about the effectiveness of EV as well as the concerns over the phishing protection. Google makes the [same change](https://groups.google.com/a/chromium.org/d/topic/security-dev/h1bTcoTpfeI/discussion) to Chrome 77 shipping on September 10.

Some users may be expecting that the indicator with a company name appears whenever they visit the trusted website. If your site uses an EV SSL certificate, let the customer support team know of the change so they can prepare an answer to potential questions from clients. If your online help centre has an article about the EV indicator displayed in various browsers, it may also have to be revised.
