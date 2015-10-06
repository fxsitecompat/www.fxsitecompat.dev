---
title: "`document.execCommand` が切り取り、コピー、貼り付けで例外を投げなくなりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1012662": "Bug 1012662 - Allow document.execCommand(\"cut\"/\"copy\") to be used within the context of user generated events"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1161721": "Bug 1161721 - Return false from document.queryCommandSupported(\"paste\") if calling execCommand(\"paste\") will fail"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1162952": "Bug 1162952 - Fix document.queryCommandEnabled(\'cut\'/\'copy\') to return true always"
---
Firefox で、Web ページがユーザ生成イベントハンドラ内でクリップボードの内容を機械的に変更することが可能となりました。このため、たとえば「クリックしてコピー」のようなアクションに Flash Player などの代替策を用意する必要がなくなります。詳しくは dev-platform メーリングリストの [関連スレッド](https://groups.google.com/d/topic/mozilla.dev.platform/oWhmLMvGAD0/discussion) と [Mozilla Hacks ブログ](https://hacks.mozilla.org/2015/09/flash-free-clipboard-for-the-web/) を参照してください。

この変更によって [`document.execCommand`](https://developer.mozilla.org/ja/docs/Web/API/Document/execCommand) と [`document.queryCommandEnabled`](https://developer.mozilla.org/ja/docs/Web/API/Document/queryCommandEnabled) の実装が更新されました。これらのメソッドは `cut` および `copy` について例外を投げなくなり、ユーザ生成イベントハンドラ内では `true` を、その他の場合は `false` を返すようになりました。`paste` コマンドはセキュリティ上の理由から今後も使用できず、これらのメソッドは `false` を返します。[`document.queryCommandSupported`](https://developer.mozilla.org/ja/docs/Web/API/Document/queryCommandSupported) メソッドは、常に `true` を返す代わりに正しい値を返すようになりました。
