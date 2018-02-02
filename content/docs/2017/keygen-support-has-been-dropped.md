---
draft: true
title: "`<keygen>` support has been dropped"
date: "2017-12-26T11:12:00-05:00"
categories: ["dom", "html", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315460"
      title: "Bug 1315460 - Remove support for HTML Keygen"
---
The support for the non-standard [`<keygen>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/keygen) HTML element and [`HTMLKeygenElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLKeygenElement) DOM interface has been removed with Firefox 60. This public key generator functionality was never implemented by Internet Explorer and Google Chrome has already removed the support with [version 57](https://www.chromestatus.com/feature/5716060992962560) shipped in March 2017. Use the standard [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API) instead.
