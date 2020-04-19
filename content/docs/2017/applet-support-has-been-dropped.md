---
title: "`<applet>` support has been dropped"
date: "2017-07-13T21:19:00-04:00"
categories: ["dom", "html", "plugins"]
tags: []
versions: ["56", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1279218"
      title: "Bug 1279218 - Remove <applet> element"
aliases:
    - "/en-CA/docs/2016/applet-support-will-be-removed/"
---
The support for the deprecated [`<applet>`](https://developer.mozilla.org/docs/Web/HTML/Element/applet) HTML element and `HTMLAppletElement` DOM interface has been removed with Firefox 56, making it an [`HTMLUnknownElement`](https://developer.mozilla.org/docs/Web/API/HTMLUnknownElement). The Java plug-in support has already been dropped with [Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) except for the ESR channel for enterprise users. The [`document.applets`](https://developer.mozilla.org/docs/Web/API/Document/applets) DOM property will be kept for backward compatibility but always return an empty collection.
