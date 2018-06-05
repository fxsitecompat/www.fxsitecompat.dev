---
title: "`<keygen>` support will be dropped"
date: "2018-06-05T10:31:00-04:00"
categories: ["dom", "html", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315460"
      title: "Bug 1315460 - Remove support for HTML Keygen"
aliases:
    - "/en-CA/docs/2017/keygen-support-has-been-dropped/"
---
The support for the non-standard [`<keygen>`](https://developer.mozilla.org/docs/Web/HTML/Element/keygen) HTML element and [`HTMLKeygenElement`](https://developer.mozilla.org/docs/Web/API/HTMLKeygenElement) DOM interface will be removed in the near future. This public key generator functionality was never implemented by Internet Explorer and Google Chrome has already removed the support with [version 57](https://www.chromestatus.com/feature/5716060992962560) shipped in March 2017. Use the standard [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) instead.
