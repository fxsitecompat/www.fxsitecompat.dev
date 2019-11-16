---
title: "既定の HTTP `Accept` ヘッダーに `image/webp` が追加されました"
date: "2019-11-16T11:43:00-05:00"
categories: ["networking"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1544231"
      title: "Bug 1544231 - Missing 'image/webp' in default navigation value of the 'Accept' header"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/UTHTGok5x4o/discussion"
      title: "Intent to ship: Add image/webp to default Accept header"
---
[Firefox 65](https://www.fxsitecompat.dev/ja/docs/2018/webp-image-support-has-been-added/) で WebP 画像対応が導入された際、既定のナビゲーション (通常の HTML ページ読み込み) と画像双方の HTTP `Accept` リクエストヘッダーに `image/webp` が追加されました。その後、値が [Fetch 仕様](https://fetch.spec.whatwg.org/#fetching) に準拠していないという理由で、Firefox 66 でそれは既定の `Accept` ヘッダーから削除されました。

仕様は未だに変わっていないものの、Google Chrome は `image/webp` を送信し続けており、様々なサイトがそれをサーバーサイド WebP 対応判別に使用していることから、Firefox 72 で再度既定の `Accept` ヘッダーに `image/webp` が追加されました。新たな値は以下のようになります。

```
text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
```
