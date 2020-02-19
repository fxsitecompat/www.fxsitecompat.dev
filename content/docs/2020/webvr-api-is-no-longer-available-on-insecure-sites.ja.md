---
title: "WebVR API が安全でないサイト上では使用できなくなりました"
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
    - "/ja/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/"
    - "/ja/docs/2018/webvr-will-not-be-available-on-insecure-sites/"
---
Firefox 73 以降、[WebVR API](https://developer.mozilla.org/docs/Web/API/WebVR_API) は、HTTPS 経由で配信された安全なサイトのみで動作するようになります。これは、この API が繊細なセンサー入力を露呈しているためです。安全でないサイト上では、関連インターフェイス、メソッド、プロパティは `undefined` となります。たとえデモとしてであっても何らかの WebVR コンテンツを提供している場合は、必ず HTTPS で配信しましょう。
