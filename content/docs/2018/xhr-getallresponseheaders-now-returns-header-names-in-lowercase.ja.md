---
title: "`XHR.getAllResponseHeaders()` がヘッダー名を小文字で返すようになりました"
date: "2018-09-27T15:18:00-04:00"
categories: ["dom"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398718"
      title: "Bug 1398718 - Remove default pref-off for lowercase header names in XHR.getAllResponseHeaders()"
---
Firefox 64 以降、[`XMLHttpRequest.getAllResponseHeaders`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/getAllResponseHeaders) メソッドは、現行の XMLHttpRequest 仕様に従って HTTP ヘッダー名を小文字で返します。Mozilla は一度 Firefox 55 でこの変更を行おうとしましたが、いくつかの互換性問題が原因で Nightly 開発サイクル中に取り消されていました。現時点では、[Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=716994) と [Safari](https://bugs.webkit.org/show_bug.cgi?id=169286) が既に変更を行っていることから、互換性リスクは低いはずです。
