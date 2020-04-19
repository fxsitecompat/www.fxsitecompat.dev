---
title: "`document.domain` 設定時にポートが変更されず、パーミッションエラーを引き起こす可能性があります"
date: "2016-09-25T01:23:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
releases: ["48"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1292522"
      title: "Bug 1292522 - with document.domain set on iframe/parent, permission denied on property-access across frame/parent when coming from different ports"
---
[`document.domain`](https://developer.mozilla.org/docs/Web/API/Document/domain) プロパティは設定可能であり、それによって、一般的に親ページと `<iframe>` ページの組み合わせのような、異なるサブドメインにあるドキュメントが互いに応答することが可能です。このようにして [オリジンを変更](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy#Changing_origin) した場合、そのドキュメントのポート番号は `null` となります。しかし Firefox 48 ではポート番号が上書きされず、そのため異なるポート上にあるドキュメントは `document.domain` で同一ポートを設定していない限り相互にアクセスできません。同一オリジンポリシー違反による「permission denied」エラーを引き起こしていたこのリグレッションは Firefox 49 で修正されました。
