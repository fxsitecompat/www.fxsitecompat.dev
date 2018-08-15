---
title: "`navigator.platform` が 64 ビット版 Firefox 上でも `\"Win32\"` を返すようになりました"
date: "2018-08-14T03:35:00-04:00"
categories: ["misc"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1472618"
      title: "Bug 1472618 - navigator.platform returns \"Win64\" in Firefox on Win64 OS but \"Win32\" in Chrome and Edge"
---
Firefox 63 以降、[`navigator.platform`](https://developer.mozilla.org/docs/Web/API/NavigatorID/platform) プロパティは、64 ビット版 Firefox を含むすべての Windows プラットフォーム上で  `"Win32"` を返します。この変更は、64 ビット版 Google Chrome と 64 ビット版 Microsoft Edge がいずれも意図的に `"Win32"` を返していることを踏まえ、潜在的なウェブ互換性問題を防ぐために行われました。一方、`navigator.oscpu` と `navigator.userAgent` は今後も実際のプラットフォームを露呈します。
