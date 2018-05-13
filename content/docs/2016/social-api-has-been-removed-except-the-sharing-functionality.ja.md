---
title: "共有機能以外の Social API が削除されました"
date: "2016-08-15T14:58:00-04:00"
categories: ["misc"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1289549"
      title: "Bug 1289549 - SocialAPI deprecation"
---
[各種サービスプロバイダー](https://activations.cdn.mozilla.net/ja/) によって実装されている [ページ共有機能](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API/Share) を除く非標準 [Social API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API) の大半が削除されました。この Firefox 固有の API は、[Facebook メッセンジャー](https://www.mozilla.jp/blog/entry/10050/) のようなソーシャル機能をアドオンに依存することなくブラウザーへ統合するため、[2012 年に導入されました](https://blog.mozilla.org/labs/2012/03/experimenting-with-social-features-in-firefox/)。しかし、積極的に紹介されたり広く利用されたりすることはなく、今回の廃止に至りました。Mozilla はサイドバーを提供していて影響を受ける少数のプロバイダーに対して既に通知を行っています。
