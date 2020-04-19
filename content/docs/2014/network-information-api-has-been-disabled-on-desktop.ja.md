---
title: "デスクトップで Network Information API が無効化されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1020758"
      title: "Bug 1012944 – [Network Information API] Disable the API on desktop"
---
`navigator.mozConnection` として実装されている [Network Information API](https://developer.mozilla.org/docs/Web/API/Network_Information_API) が、デスクトップ版 Firefox で意図せず露呈されていたことから無効化されました。現在のところこの API は Android 版 Firefox と Firefox OS のみで動作します。
