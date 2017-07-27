---
title: "Application Cache API が廃止予定となりました"
date: "2015-09-25T01:55:00-04:00"
categories: ["html"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1204581"
      title: "Bug 1204581 - Add a deprecation notice for AppCache if service worker fetch interception is enabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1163545"
      title: "Bug 1163545 - Bypass AppCache completely when Service Workers supported & registered"
---
ウェブアプリケーションの [オフライン対応](https://developer.mozilla.org/ja/Apps/Build/Offline) を可能にする HTML5 の [Application Cache API](https://developer.mozilla.org/ja/docs/Web/HTML/Using_the_application_cache) (AppCache) が廃止予定と見なされ、[将来的に Firefox から削除されることとなりました](https://www.fxsitecompat.com/ja/docs/2016/application-cache-support-will-be-removed/)。ウェブ開発者の皆さんには、代替策として [Service Workers](https://developer.mozilla.org/ja/docs/Web/API/Service_Worker_API) を学ぶことをお勧めします。それによって、よりリッチでシームレスなオフラインユーザー体験を近いうちに提供できるようになります。この新しい API は、まだすべての機能が実装されているわけではありませんが、既に [Firefox Developer Edition](https://www.mozilla.org/ja/firefox/developer/) でテスト可能となっています。なお、Service Worker が登録されている場合、AppCache は無視されます。

**更新**: Service Worker API は Firefox 44 で正式公開となり、Beta、Release 両チャンネルでも利用可能となりました。
