---
title: "`-moz-text-blink` が削除され、`-moz-text-decoration-line:blink` に置き換えられました"
date: "2013-09-19T23:58:13-04:00"
categories: ["css"]
tags: []
releases: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=812995"
      title: "Bug 812995 – add \'blink\' to -moz-text-decoration-line and drop -moz-text-blink"
aliases:
    - "/ja/docs/2013/moz-text-blink-has-been-removed-in-favor-of-moz-text-decoration-line-blink/"
---
非標準の [`-moz-text-blink`](https://developer.mozilla.org/docs/Web/CSS/-moz-text-blink) プロパティが削除されました。その代わり、標準となったもののまだ接頭辞付きの [`text-decoration-line`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-line) プロパティが `blink` を正当な値として取るようになりました。ただし実際のところ、[アクセシビリティ](https://developer.mozilla.org/docs/Accessibility) への配慮から、Firefox 上ではコンテンツは一切点滅しません。なお、`text-decoration:blink` による点滅効果は [Firefox 23 で削除されています](https://www.fxsitecompat.dev/ja/docs/2013/blink-effect-with-text-decoration-blink-has-been-dropped/)。
