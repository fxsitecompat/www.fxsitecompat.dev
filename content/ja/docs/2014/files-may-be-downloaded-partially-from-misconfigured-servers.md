---
title: "サーバの誤設定によりファイルが部分的にダウンロードされる場合があります "
date: "2014-07-22T05:06:26-04:00"
categories: ["networking"]
tags: []
versions: ["33"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083090"
      title: "Bug 1083090 – Broken CSS and JavaScript errors with Firefox 33 (regression) [partial transfer]"
---
Firefox 33 で導入された HTTP 1.1 以降のための適切なフレーミング検査により、誤った設定が行われている Web サーバから、JavaScript、CSS、CSV、PDF、その他の種類のファイルが一部のみしか転送されないことが判明しています。最初のケースは、`Content-Encoding: gzip` ヘッダが設定されている一方、`Content-Length` ヘッダに間違ったサイズが書かれているというものです。Apache サーバでは、適切な解決策ではないものの、`mod_deflate` モジュールを無効化することで問題を素早く回避できます。別のケースは、チャンク転送エンコーディングのレスポンスにおいて終端のゼロチャンクが欠落しているというものです。これらの相互運用性問題は Firefox 33.1 で修正され、フレーミング検査は SPDY と HTTP/2 以降のみに強制されるようになります。
