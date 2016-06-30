---
title: "Flash が「クリックして有効化」時は `navigator.plugins` や `navigator.mimeTypes` に列挙されなくなりました"
date: "2016-06-30T17:20:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove Flash from navigator.plugins when it's click-to-play"
aliases:
    - "/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
    - "/docs/2016/navigator-plugins-no-longer-lists-click-to-activate-plug-ins/"
    - "/docs/2016/navigator-plugins-no-longer-lists-flash-when-it-s-click-to-activate/"
---
Firefox 50 以降、Adobe Flash Player プラグインが「[クリックして有効化](https://developer.mozilla.org/ja/Add-ons/Plugins/Site_Author_Guide_for_Click-To-Activate_Plugins)」するよう設定されている場合、[`navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/plugins)、[`navigator.mimeTypes`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/mimeTypes) 両プロパティに含まれなくなりました。多くのサイトは Flash が判別できない時は代わりに HTML5 動画を提供していることから、この変更は Flash を手作業で有効化する必要のあった場面においてユーザ体験を改善するものと期待されています。今のところ他のプラグインに変更はありません。

**更新**: この変更は 49 Aurora チャンネル (Firefox 49 Developer Edition) へ入る直前に取り消されました。[Flash の有効化が機能しなくなった](https://bugzilla.mozilla.org/show_bug.cgi?id=1277832) ことと、[*Hulu*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277760) や [*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277825) で動画が再生されなくなったことが原因です。Mozilla 開発者がこれらの問題を調査しています。

**更新**: 上記のバグが修正され、当該パッチは Firefox 50 へ再投入されました。私たちはこのドキュメントを更新し、`navigator.mimeTypes` も影響を受けることを記載しました。
