---
title: "WebVR will not be available on insecure sites"
date: "2018-06-05T10:36:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1381645"
      title: "Bug 1381645 - Restrict access to WebVR to HTTPS only sites."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/bU2gil1SHkY/discussion"
      title: "Intent to remove: WebVR on insecure contexts"
aliases:
    - "/en-CA/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/"
---
The [WebVR API](https://developer.mozilla.org/docs/Web/API/WebVR_API) will only work on secure sites served over HTTPS in the near future, because the API exposes sensitive sensor inputs. Websites providing any WebVR content even as a demo should be using HTTPS if they have not switched yet.
