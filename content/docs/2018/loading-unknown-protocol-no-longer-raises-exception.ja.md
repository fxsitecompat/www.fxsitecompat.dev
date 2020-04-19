---
title: "未知のプロトコルの読み込みが例外を発生させなくなりました"
date: "2018-10-23T12:18:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=680300"
      title: "Bug 680300 - Restrict discoverability of protocol handlers [Tor 1623]"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/0KgeG3058NY/discussion"
      title: "Intent to implement: Suppress exception/error reporting when loading an unknown external protocol"
---
Firefox は従来、画像、フレームなどで未知の外部プロトコルを読み込もうとした際に `NS_ERROR_UNKNOWN_PROTOCOL` 例外を投げていました。バグに投稿された以下の HTML コードスニペットは、特定のブラウザー拡張機能がインストールされているかどうかによって警告ダイアログを表示します。

```html
<img src="sacore:green.gif"
     onerror="alert('McAfee Site Advisor not Installed.')"
     onload="alert('McAfee Site Advisor Installed!')">
```

これはフィンガープリンティング要因となる可能性があることや他のブラウザーがエラーを報告していないことから、ユーザープライバシー保護強化のため Firefox 64 以降では例外が投げられなくなりました。
