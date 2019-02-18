---
title: "サードパーティトラッキング Cookie が初期設定でブロックされるようになりました"
date: "2018-11-22T01:28:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["65"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492549"
      title: "Bug 1492549 - Enable blocking access to storage from tracking resources by default on all desktop platforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492563"
      title: "Bug 1492563 - Enable blocking access to storage from tracking resources by default on all desktop platforms on Nightly"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oFZivEmLC40/discussion"
      title: "Intent to implement and ship: New cookie jar policy to block storage access from tracking resources"
aliases:
    - "/ja/docs/2015/third-party-cookies-may-be-disabled-by-default-in-the-future/"
---
Firefox 65 で、すべてのデスクトッププラットフォームにおいて [コンテンツブロッキング](https://support.mozilla.org/kb/content-blocking) が初期設定有効となりました。これにより、今後ブラウザー上で、サードパーティトラッキング Cookie を含むトラッキングリソースによるストレージアクセスがブロックされます。

サードパーティ Cookie のブロックは当初 [Firefox 22](https://www.fxsitecompat.com/ja/docs/2013/third-party-cookies-are-blocked-by-default/) で予定されていましたが、明らかな互換性問題から変更は取り消されていました。その後 2015 年になり、[Firefox 42](https://fxsitecompat.com/ja/docs/2015/private-browsing-now-comes-with-tracking-protection/) でプライベートブラウジングモード内のトラッキング防止機能が導入され、次いで [Firefox Focus](https://blog.mozilla.org/blog/2015/12/07/focus-by-firefox-content-blocking-for-the-open-web/) が公開されました。両製品とも [Disconnect の公開ブラックリスト](https://github.com/disconnectme/disconnect-tracking-protection) を用いて、広告トラッカー、アクセス解析コード、ソーシャル共有ボタンなどのトラッキングリソースを特定しています。

Apple が Safari に [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/) を追加する一方、Mozilla は [姿勢を変え](https://blog.mozilla.org/futurereleases/2018/08/30/changing-our-approach-to-anti-tracking/)、[iOS 版 Firefox](https://blog.mozilla.org/blog/2018/04/12/latest-firefox-for-ios-now-available-with-tracking-protection-by-default/) を手始めとしてトラッキング防止機能を初期設定で有効化することとしました。この機能は、現在ではコンテンツブロッキングと呼ばれていますが、Firefox 63 以降 Beta チャンネルで試験されており、Firefox 64 以降 Nightly チャンネルでは初期設定で有効化されいます。

ウェブ開発者やサイト運営者の皆さんは、コンテンツブロッキングが有効の状態ですべてのサイト機能が正しく動作することを確認してください。まずは Mozilla のプライバシーエンジニアによって書かれた [ストレージアクセスポリシー文書](https://developer.mozilla.org/docs/Mozilla/Firefox/Privacy/Storage_access_policy) を読んでみましょう。Mozilla はまた、埋め込み [動画](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1400025)、[画像](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1470301)、[コメント](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1486425) および [ログイン](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1470298) に関する問題を追跡しており、これらは一般的な間違いを把握するのに役立つかもしれません。

**更新**: この変更は [Firefox 65 では取り消され](https://bugzilla.mozilla.org/show_bug.cgi?id=1514853)、[Firefox 66 に向けた再試行](https://bugzilla.mozilla.org/show_bug.cgi?id=1525727) もバックアウトされています。私たちは今後の変更の監視を続けます。
