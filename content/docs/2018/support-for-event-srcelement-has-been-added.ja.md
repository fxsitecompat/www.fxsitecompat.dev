---
title: "`Event.srcElement` への対応が追加されました"
date: "2018-05-08T16:17:00-04:00"
categories: ["dom"]
tags: []
versions: ["62"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=453968"
      title: "Bug 453968 - Support IE extension Event.srcElement"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1339000"
      title: "Bug 1339000 - Some content is not shown on qq.com, due to use of event.srcElement"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1444004"
      title: "Bug 1444004 - Implement Event.srcElement on nightly only for now"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/y9KU21IBFvo/discussion"
      title: "Intent to ship: event.srcElement"
aliases:
    - "/ja/docs/2018/support-for-event-prototype-srcelement-has-been-added/"
---
Firefox は、クロスブラウザー互換性を高める目的で、`Event` インターフェイス上の非標準 [`srcElement`](https://developer.mozilla.org/docs/Web/API/Event/srcElement) プロパティに対応しました。Firefox Nightly はバージョン 60 以降既に対応を追加しています。これは Internet Explorer に由来する標準 [`target`](https://developer.mozilla.org/docs/Web/API/Event/target) プロパティのエイリアスですが、これまでに他のすべてのブラウザーが実装しています。

Mozilla のエンジニアは、これが Firefox を対象としたブラウザー判別に誤用されていた場合に正常に動作しなくなるサイトが発生することを懸念しています。あなたのサイトがそのような状況に該当しないよう確認してください。

**更新**: この変更により *QQ.com* で一部のコンテンツが表示されていません。
