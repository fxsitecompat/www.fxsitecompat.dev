---
title: "UA 文字列が 64 ビット版 OS 上で 32 ビット版 Firefox が実行されている事実を示さなくなりました"
date: "2019-07-07T01:03:00-04:00"
categories: ["networking"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1559747"
      title: "Bug 1559747 - User-Agent string needn't reveal a user is running 32-bit Firefox on a 64-bit OS"
---
これまで Firefox のユーザーエージェント (UA) 文字列は、「WOW64」や「Linux i686 on x86_64」といったように、ユーザーが 64 ビットオペレーティングシステム上で 32 ビット版 Firefox を実行している事実を露呈していました。これは特に Adobe Flash Player とのブラウザー互換性を判別するために必要とされていましたが、現在のプラグインインストーラーには 32 ビット版と 64 ビット版どちらも含まれており、いずれにしても [Flash Player は廃止予定となっています](https://www.fxsitecompat.dev/ja/docs/2018/flash-plug-in-support-will-be-removed-in-2020/)。

Firefox 69 でこうした追加情報が UA 文字列から削除され、`User-Agent` HTTP リクエストヘッダーや `navigator.userAgent`、`navigator.platform`、`navigator.oscpu` DOM API では単に「Win64」あるいは「Linux x86_64」と表記されるようになりました。

この変更により、UA フィンガープリンティング要因が削減されるとともに、ユーザーが 32 ビット版 Firefox を使っている場合でも 64 ビット OS には 64 ビット版アプリケーションを配信すべきソフトウェアダウンロードサイトにおける UX の向上が期待されています。
