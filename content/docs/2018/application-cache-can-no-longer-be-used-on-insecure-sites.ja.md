---
title: "アプリケーションキャッシュが安全でないサイトでは使用できなくなりました"
date: "2018-05-10T12:54:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460478"
      title: "Bug 1460478 - Disable support for AppCache over insecure contexts for stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qLTTpdzcDkw/discussion"
      title: "Intent to Unship: Application Cache over Insecure Contexts"
    - url: "https://blog.mozilla.org/security/2018/02/12/restricting-appcache-secure-contexts/"
      title: "Mozilla Security Blog: Restricting AppCache to Secure Contexts"
---
Firefox 62 以降、[HTML5 アプリケーションキャッシュ](https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache) (AppCache) を非 HTTPS サイトで使用することは不可能となり、そうしたサイトではキャッシュマニフェストは無視され、`window.applicationCache` は `undefined` となります。このセキュリティ制限は [バージョン 60](https://www.fxsitecompat.com/ja/docs/2018/support-for-application-cache-on-insecure-sites-has-been-deprecated/) 以降の Firefox Nightly と早期 Beta/DevEdition には既に導入されています。

なお、AppCache は [Firefox 44 以降廃止予定](https://www.fxsitecompat.com/ja/docs/2015/application-cache-api-has-been-deprecated/) とされており、
より高機能で当初から HTTPS サイトでのみ使用可能な [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) に取って代わられる形で、将来的は完全に [廃止されます](https://www.fxsitecompat.com/ja/docs/2016/application-cache-support-will-be-removed/)。
