---
title: "安全でないサイトでの Application Cache 対応が廃止予定となりました"
date: "2018-02-02T01:29:00-05:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354175"
      title: "Bug 1354175 - Remove access to AppCache in insecure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qLTTpdzcDkw/discussion"
      title: "Intent to Unship: Application Cache over Insecure Contexts"
    - url: "https://blog.mozilla.org/security/2018/02/12/restricting-appcache-secure-contexts/"
      title: "Mozilla Security Blog: Restricting AppCache to Secure Contexts"
---
現在進行中の [安全でない HTTP 廃止](https://www.fxsitecompat.com/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、Firefox 60 Nightly と早期 Beta/DevEdition では、非 HTTPS サイト上での Application Cache (AppCache) の使用が許可されなくなります。無効化された場合、キャッシュマニフェストファイルは無視され `window.applicationCache` は `undefined` となります。特に大きな問題がなければ、Firefox 62 ですべてのチャンネルにおいてこの変更が行われます。

なお、AppCache 対応自体 [Firefox 44 以降廃止予定](https://www.fxsitecompat.com/ja/docs/2015/application-cache-api-has-been-deprecated/) となっており、より高機能な Service Worker API に取って代わられる形で将来的に完全に [削除されます](https://www.fxsitecompat.com/ja/docs/2016/application-cache-support-will-be-removed/)。

**更新**: 予定通り、[Firefox 62](https://www.fxsitecompat.com/ja/docs/2018/application-cache-can-no-longer-be-used-on-insecure-sites/) 以降すべてのチャンネルで制約が課されます。
