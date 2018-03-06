---
draft: true
title: "WebVR can no longer be used on insecure sites"
date: "2017-12-07T18:00:00-05:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1381645"
      title: "Bug 1381645 - Restrict access to WebVR to HTTPS only sites."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/bU2gil1SHkY/discussion"
      title: "Intent to remove: WebVR on insecure contexts"
---
Starting with Firefox 61, the [WebVR API](https://developer.mozilla.org/en-US/docs/Web/API/WebVR_API) available since Firefox 55 will only work on secure sites served over HTTPS, since the API exposes sensitive sensor inputs. Websites providing any WebVR content even as a demo should be using HTTPS if they have not switched yet.
