---
title: "Application Cache 対応が廃止されます"
date: "2016-01-08T00:06:00-05:00"
categories: ["html"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782": "Bug 1237782 - Remove support for appcache"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1163545": "Bug 1163545 - Bypass AppCache completely when Service Workers supported & registered"
---
[Firefox 44 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2015/application-cache-api-has-been-deprecated/) [Application Cache API](https://developer.mozilla.org/ja/docs/Web/HTML/Using_the_application_cache) (AppCache) への対応は、よりリッチなオフライン体験を可能にする [Service Workers API](https://developer.mozilla.org/ja/docs/Web/API/Service_Worker_API) に置き換えられる形で、将来的に削除されます。AppCache は古いブラウザ向けのフォールバックとして引き続き使用できますが、Service Worker が登録されている場合にはいずれにしても無視されます。この新しい API で何ができるかは [Service Worker Cookbook](https://serviceworke.rs/) をご覧ください。
