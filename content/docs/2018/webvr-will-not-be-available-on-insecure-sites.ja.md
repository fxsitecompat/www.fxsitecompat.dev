---
title: "WebVR が安全でないサイト上では使用できなくなります"
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
    - "/ja/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/"
---
[WebVR API](https://developer.mozilla.org/docs/Web/API/WebVR_API) は、近々 HTTPS 経由で配信された安全なサイトのみで動作するようになります。これは、この API が繊細なセンサー入力を露呈しているためです。たとえデモとしてであっても何らかの WebVR コンテンツを提供しているウェブサイトは、もしまだ移行していなければ HTTPS を採用しなければなりません。
