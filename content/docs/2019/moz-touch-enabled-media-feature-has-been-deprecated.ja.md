---
title: "`-moz-touch-enabled` メディア特性が廃止予定となりました"
date: "2019-10-20T13:19:00-04:00"
categories: ["css"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035774"
      title: "Bug 1035774 - Implement Interaction Media Features including pointer:coarse that replaces non-standard -moz-touch-enabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1588737"
      title: "Bug 1588737 - The user is unable to scroll on feedmusic.com on Yoga devices (caused by Modernizr.touch having different values in Firefox vs. Chrome, caused by -moz-touch-enabled)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SPmSiWfn1Ts/discussion"
      title: "Intent to unship: @media (-moz-touch-enabled)"
---
[`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) CSS メディア特性が Firefox 71 以降の Nightly チャンネルで無効化され、近い将来すべてのチャンネルから削除されることとなりました。標準の [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) が Firefox 64 以降使用可能となっている上、この非標準メディア特性を用いた *Modernizr* ライブラリの誤判別により少なくとも 1 つのサイトが Firefox 上でスクロールできない問題が判明していることから、この廃止予定が決まりました。

代わりとしては [`pointer`](https://developer.mozilla.org/docs/Web/CSS/@media/pointer) メディア特性を使用することができます。例えば、あなたのサイトのメディアクエリーに `-moz-touch-enabled:1` が含まれている場合、単純に `pointer:coarse` で置き換えてください。

これは Firefox に最後まで残った非標準システム測定メディア特性です。他のものは既に [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/non-standard-system-metric-pseudo-classes-and-media-features-have-been-removed/) で削除されています。

**更新**: このメディア特性は [Firefox 73](https://www.fxsitecompat.dev/ja/docs/2019/moz-touch-enabled-media-feature-has-been-removed/) で廃止されました。
