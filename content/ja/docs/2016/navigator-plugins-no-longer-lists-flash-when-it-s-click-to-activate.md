---
title: "Flash が「クリックして有効化」時は `navigator.plugins` に列挙されなくなりました"
date: "2016-06-01T16:39:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove Flash from navigator.plugins when it's click-to-play"
aliases:
    - "/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
    - "/docs/2016/navigator-plugins-no-longer-lists-click-to-activate-plug-ins/"
---
Firefox 49 以降、Adobe Flash Player プラグインが「[クリックして有効化](https://developer.mozilla.org/ja/Add-ons/Plugins/Site_Author_Guide_for_Click-To-Activate_Plugins)」するよう設定されている場合、[`navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/plugins) プロパティによって返される [`PluginArray`](https://developer.mozilla.org/ja/docs/Web/API/PluginArray) に含まれなくなりました。多くのサイトは Flash が判別できない時は代わりに HTML5 動画を提供していることから、この変更は Flash を手作業で有効化する必要のあった場面においてユーザ体験を改善するものと期待されています。今のところ他のプラグインは影響を受けません。

**更新**: この変更は Aurora チャンネル (Developer Edition) へ入る直前に取り消されました。[Flash の有効化が機能しなくなった](https://bugzilla.mozilla.org/show_bug.cgi?id=1277832) ことと、[*Hulu*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277760) や [*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277825) で動画が再生されなくなったことが原因です。Mozilla 開発者がこれらの問題を調査しています。
