---
title: "専用ワーカーは、埋め込み型を除き、親ドキュメントから CSP を継承しなくなりました"
date: "2016-03-13T11:59:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1223647"
      title: "Bug 1223647 - CSP erroneously \"inherited\" into dedicated workers"
---
[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) か [`importScripts`](https://developer.mozilla.org/ja/docs/Web/API/WorkerGlobalScope/importScripts) が使われている場合に、[専用ワーカー](https://developer.mozilla.org/ja/docs/Web/API/Web_Workers_API/Using_web_workers#Dedicated_workers) が誤って親ドキュメントのポリシーを「継承」しているという [Content Security Policy](https://developer.mozilla.org/ja/docs/Web/Security/CSP) (CSP) の実装バグが Firefox 45 で修正されました。

一方、[埋め込みワーカー](https://developer.mozilla.org/ja/docs/Web/API/Web_Workers_API/Using_web_workers#Embedded_workers) は親ポリシーを継承しますが、[`Blob`](https://developer.mozilla.org/ja/docs/Web/API/Blob/Blob) に `text/javascript` など有効なスクリプト用 MIME タイプを指定する必要があります。そうしないと、`script-src` の代わりに `default-src` ディレクティブがそのワーカーに適用され、予期せぬ CSP エラーにつながる可能性があります。この制約により [*Yandex.Disk* が Firefox 45 で正しく動作していません](https://bugzilla.mozilla.org/show_bug.cgi?id=1256148)。

**Update**: *Yandex.Disk* の問題は Yandex チームによって修正されました。
