---
draft: true
title: "`<keygen>` 対応が廃止されました"
date: "2017-12-26T11:12:00-05:00"
categories: ["dom", "html", "privacy-security"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315460"
      title: "Bug 1315460 - Remove support for HTML Keygen"
---
非標準の [`<keygen>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/keygen) HTML 要素と [`HTMLKeygenElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLKeygenElement) DOM インターフェイスへの対応は Firefox 61 で削除されました。この公開鍵生成機能は Internet Explorer では一度も実装されたことがなく、Google Chrome は 2017 年 3 月公開の [バージョン 57](https://www.chromestatus.com/feature/5716060992962560) で既に対応を廃止しています。代わりに標準の [Web Crypto API](https://developer.mozilla.org/ja/docs/Web/API/Web_Crypto_API) を使用してください。
