---
title: "EV SSL 証明書インジケーターがロケーションバーから削除されました"
date: "2019-09-04T22:40:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1572936"
      title: "Bug 1572936 - Move EV cert UI out of URL Bar"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o18n0SZRyUE/discussion"
      title: "Intent to Ship: Move Extended Validation Information out of the URL bar"
    - url: "https://blog.mozilla.org/security/2019/10/15/improved-security-and-privacy-indicators-in-firefox-70/"
      title: "Mozilla Security Blog: Improved Security and Privacy Indicators in Firefox 70"
---
これはサイト互換性問題ではなくむしろユーザー体験に関するトピックですが、Firefox 70 以降、Extended Validation (EV) SSL 証明書インジケーターがロケーションバー内に表示されなくなったことについて、ここで触れておくべきかと考え記事にしました。この変更は EV の有用性に関する疑念やフィッシング対策に関する懸念に基づいたもので、Google も 9 月 10 日公開の Chrome 77 で [同様の変更](https://groups.google.com/a/chromium.org/d/topic/security-dev/h1bTcoTpfeI/discussion) を行っています。

一部のユーザーは、信頼できるウェブサイトを訪れるたびに、企業名の書かれたインジケーターが表示されることを期待しているかもしれません。あなたのサイトが EV SSL 証明書を使用している場合は、この変更をカスタマーサポートチームに知らせて、彼らが顧客からの潜在的な質問への回答を準備できるようにしましょう。また、各種ブラウザー内に表示される EV インジケーターに関する記事がオンラインのヘルプセンターに存在する場合は、それも改訂する必要があるかもしれません。
