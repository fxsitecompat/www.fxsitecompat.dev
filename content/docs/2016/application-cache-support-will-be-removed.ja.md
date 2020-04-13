---
title: "Application Cache 対応が廃止されます"
date: "2016-01-08T00:06:00-05:00"
categories: ["html"]
tags: []
versions: ["77"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782"
      title: "Bug 1237782 - Remove support for appcache"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1619673"
      title: "Bug 1619673 - Disable appcache in release"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5JqnS_PnKqU/discussion"
      title: "Intent to unship AppCache"
---
[Firefox 44 以降廃止予定となっている](https://www.fxsitecompat.dev/ja/docs/2015/application-cache-api-has-been-deprecated/) [Application Cache API](https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache) (AppCache) への対応は、よりリッチなオフライン体験を可能にする [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) に置き換えられる形で、将来的に削除されます。AppCache は古いブラウザー向けのフォールバックとして引き続き使用できますが、Service Worker が登録されている場合にはいずれにしても無視されます。現時点で Firefox から AppCache 対応を削除する具体的なスケジュールはまだ立っていませんが、今のうちからこの新しい API について学ぶことが得策でしょう。[Service Worker Cookbook](https://serviceworke.rs/) に様々な有用な例が載っています。

**更新**: Service Worker API は Firefox 44 で正式公開となり、Beta、Release 両チャンネルでも利用可能となりました。

**更新 2**: AppCache 対応は 2020 年 6 月 2 日公開の Firefox 77 で [削除される見通しです](https://groups.google.com/d/msg/mozilla.dev.platform/5JqnS_PnKqU/8jGozKS1AAAJ)。Google も 6 月 23 日公開の Chrome 84 での削除を予定しています。
