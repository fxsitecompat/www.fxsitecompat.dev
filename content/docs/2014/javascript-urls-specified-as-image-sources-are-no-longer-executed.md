---
title: "`javascript` URLs specified as image sources are no longer executed"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1018583"
      title: "Bug 1018583 – <style>background: url(\'javascript:while(true){}\');</style> hangs Firefox"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/UsspiA5a3Ok/discussion"
      title: "Intent to unship: javascript: execution outside navigation contexts"
---
Previously, `javascript` URLs specified as [`<img>`](https://developer.mozilla.org/docs/Web/HTML/Element/img)`src` or CSS background images were parsed and executed as normal JavaScript codes. This trick no longer works, because it could be exploited to hang the browser, leading to a denial of service (DoS) attack.
