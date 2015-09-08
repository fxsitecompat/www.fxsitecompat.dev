---
title: "`javascript` URLs specified as image sources are no longer executed"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: "33"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1018583": "Bug 1018583 – <style>background: url(\'javascript:while(true){}\');</style> hangs Firefox"
---
Previously, `javascript` URLs specified as [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img)`src` or CSS background images were parsed and executed as normal JavaScript codes. This trick no longer works, because it could be exploited to hang the browser, leading to a denial of service (DoS) attack.
