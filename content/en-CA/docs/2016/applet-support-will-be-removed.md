---
title: "`<applet>` support will be removed"
date: "2016-10-05T18:38:00-04:00"
categories: ["dom", "html", "plugins"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1279218"
      title: "Bug 1279218 - Remove <applet> element"
---
The support for the deprecated `HTMLAppletElement` interface will be removed once Firefox 52, excluding the ESR channel for enterprise users, [drops the support for the Java plug-in](https://www.fxsitecompat.com/en-CA/docs/2016/plug-in-support-has-been-dropped-other-than-flash/). The [`<applet>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/applet) element will be an [`HTMLUnknownElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLUnknownElement). The [`document.applets`](https://developer.mozilla.org/en-US/docs/Web/API/Document/applets) property will be kept for backward compatibility but always return an empty collection.
