---
title: "`navigator.plugins` と `mimeTypes` が列挙不能となります"
date: "2016-10-05T19:22:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=757726"
      title: "Bug 757726 - disallow enumeration of navigator.plugins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934107"
      title: "Bug 934107 - [meta] Remove use of plugin enumeration"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270364"
      title: "Bug 1270364 - MimeTypeArray should have unenumerable named properties per spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270366"
      title: "Bug 1270366 - PluginArray and Plugin should have unenumerable own properties per spec"
---
Firefox 52 で Flash 以外の [プラグイン対応が廃止](https://www.fxsitecompat.com/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) された後、それぞれ [`PluginArray`](https://developer.mozilla.org/ja/docs/Web/API/PluginArray)、`MimeTypeArray` オブジェクトを返す  [`navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/plugins)、[`navigator.mimeTypes`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/mimeTypes) 両プロパティが列挙不能となります。

この変更はフィンガープリンティングを緩和するため元々 Firefox 28 で予定されていましたが、無視できないサイト互換性問題により中止されていました。

これらのプロパティは実際のところ、[`Object.getOwnPropertyNames`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertyNames) メソッドや、単に `[...navigator.plugins]` のような [スプレッド構文](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Spread_operator) を使った場合は今後も列挙可能ですが、Flash Player がインストールされている場合にそれが含まれるだけになるので、もはや意味をなしません。
