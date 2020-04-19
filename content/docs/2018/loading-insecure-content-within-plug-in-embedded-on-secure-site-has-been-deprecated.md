---
title: "Loading insecure content within plug-in embedded on secure site has been deprecated"
date: "2018-03-09T12:04:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1441794"
      title: "Bug 1441794 - Add deprecation warning to OBJECT_SUBREQUEST for stable releases"
---
In order to tighten the [mixed content](https://developer.mozilla.org/docs/Web/Security/Mixed_content) blocking, Firefox will soon prevent a plug-in embedded on a secure, HTTPS site from loading content served from an insecure, non-HTTPS site. Firefox 60 and later will show a console warning for such cases.

Adobe Flash is the only plug-in currently supported in Firefox, and therefore this change will particularly affect loading of external XML data, which should also be served from a secure site.
