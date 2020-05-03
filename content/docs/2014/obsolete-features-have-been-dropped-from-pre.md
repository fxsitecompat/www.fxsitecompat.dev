---
title: "Obsolete features have been dropped from `<pre>`"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
releases: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949879"
      title: "Bug 949879 – Drop support for <pre cols>"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=950737"
      title: "Bug 950737 – Remove layout effect from <pre width>"
supported_tools:
  firefox_extension: true
---
The `cols` and `width` attributes of the [`pre`](https://developer.mozilla.org/docs/Web/HTML/Element/pre) element are no longer supported in Firefox. The former attribute was a non-standard extension derived from Netscape Navigator, the latter was in the HTML4 spec but removed from [HTML5](https://developer.mozilla.org/docs/Web/Guide/HTML/HTML5).
