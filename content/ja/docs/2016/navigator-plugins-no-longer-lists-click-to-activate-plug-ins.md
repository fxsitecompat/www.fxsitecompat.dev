---
title: "`navigator.plugins` に「クリックして有効化」されるプラグインが列挙されなくなりました"
date: "2016-06-01T16:39:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove plugins that are click-to-play from navigator.plugins"
aliases:
    - "/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
---
Firefox 49 以降、「[クリックして有効化](https://support.mozilla.org/ja/kb/why-do-i-have-click-activate-plugins)」するよう設定されているプラグインは、[`navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/plugins) プロパティによって返される [`PluginArray`](https://developer.mozilla.org/ja/docs/Web/API/PluginArray) に含まれなくなりました。[Firefox 47](https://www.fxsitecompat.com/ja/docs/2016/all-plug-ins-other-than-flash-are-now-defaulted-to-click-to-activate/) 以降 Flash を除くすべてのプラグインが「クリックして有効化」の対象となっていることから、「Shockwave Flash」が初期設定で列挙される唯一の項目となります。
