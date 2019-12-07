---
title: "`-moz-touch-enabled` メディア特性が廃止されました"
date: "2019-12-07T17:00:00-05:00"
categories: ["css"]
tags: []
versions: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1486964"
      title: "Bug 1486964 - Drop -moz-touch-enabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SPmSiWfn1Ts/discussion"
      title: "Intent to unship: @media (-moz-touch-enabled)"
---
[Firefox 71](https://www.fxsitecompat.dev/ja/docs/2019/moz-touch-enabled-media-feature-has-been-deprecated/) 以降廃止予定となっていた [`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) CSS メディア特性が、Firefox 73 ですべてのチャンネルから削除されました。標準の [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) が Firefox 64 以降使用可能となっている上、この非標準メディア特性を用いた *Modernizr* ライブラリの誤判別により少なくとも 1 つのサイトが Firefox 上でスクロールできない問題が判明していました。

代わりとしては [`pointer`](https://developer.mozilla.org/docs/Web/CSS/@media/pointer) メディア特性を使用することができます。例えば、あなたのサイトのメディアクエリーに `-moz-touch-enabled:1` が含まれている場合、単純に `pointer:coarse` で置き換えてください。

これは Firefox に最後まで残った非標準システム測定メディア特性でした。他のものは既に [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/non-standard-system-metric-pseudo-classes-and-media-features-have-been-removed/) で削除されています。
