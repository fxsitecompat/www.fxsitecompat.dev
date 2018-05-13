---
draft: true
title: "WebVR が安全でないサイト上では使用できなくなりました"
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
Firefox 55 以降利用可能となっている [WebVR API](https://developer.mozilla.org/docs/Web/API/WebVR_API) が、Firefox 61 以降は HTTPS 経由で配信された安全なサイトのみで動作するようになります。これは、この API が繊細なセンサー入力を露呈しているためです。たとえデモとしてであっても何らかの WebVR コンテンツを提供しているウェブサイトは、もしまだ移行していなければ HTTPS を採用しなければなりません。
