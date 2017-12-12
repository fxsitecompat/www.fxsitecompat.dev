---
title: "SMIL `accessKey` 対応が廃止されました"
date: "2017-12-12T15:31:00-05:00"
categories: ["svg"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423098"
      title: "Bug 1423098 - Remove support for SMIL's accessKey feature"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/skw-Yj_Pdjk/discussion"
      title: "Intent to unship: SMIL accessKey support"
---
Synchronized Multimedia Integration Language (SMIL) には、HTML の [`accesskey`](https://developer.mozilla.org/ja/docs/Web/HTML/Global_attributes/accesskey) 属性と同様に、特定のキーが押された際に SVG アニメーションを動かす機能が含まれています。これはウェブ開発者が `accessKey` 値を伴った `begin` 属性を用いることで定義できます。しかし、Firefox 以外どのブラウザも現時点でこの機能に対応しておらず、またこれはいくつかのセキュリティ問題の原因ともなってきました。このため、`accessKey` 対応は Firefox 59 で削除されました。
