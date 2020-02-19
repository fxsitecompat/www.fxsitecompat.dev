---
title: "WebVR API is no longer available on insecure sites"
date: "2020-02-18T19:38:00-05:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1381645"
      title: "Bug 1381645 - Restrict access to WebVR to HTTPS only sites."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1580567"
      title: "Bug 1580567 - Implement XR device access permission UI"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/bU2gil1SHkY/discussion"
      title: "Intent to remove: WebVR on insecure contexts"
aliases:
    - "/en-CA/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/"
    - "/en-CA/docs/2018/webvr-will-not-be-available-on-insecure-sites/"
---
Starting with Firefox 73, the [WebVR API](https://developer.mozilla.org/docs/Web/API/WebVR_API) will only work on secure sites served over HTTPS, because the API exposes sensitive sensor inputs. The related interfaces, methods and properties will be `undefined` on insecure sites. If you’re providing any WebVR content even as a demo, make sure to serve it via HTTPS.
