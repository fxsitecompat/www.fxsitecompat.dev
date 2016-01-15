---
title: "デスクトップ版および Android 版 Firefox から Web App Runtime が削除されます"
date: "2016-01-14T22:08:00-05:00"
categories: ["misc"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1235869": "Bug 1235869 - Remove support for WebRT"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1238079": "Bug 1238079 - disable and remove runtime"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1238576": "Bug 1238576 - Stop exposing navigator.mozApps on desktop and Android"
    "https://groups.google.com/d/topic/firefox-dev/WV2XkVN3sWQ/discussion": "firefox-dev: disabling the desktop/Android Web Runtimes"
---
Web アプリケーションをネイティブアプリケーションのようにユーザの端末へインストールし実行することを可能にしていた、非標準の [Open Web Apps JavaScript API](https://developer.mozilla.org/ja/Apps/Build/JavaScript_API) と [Web App Runtime](https://developer.mozilla.org/ja/Apps/Build/Architecture) が、[デスクトップ](https://developer.mozilla.org/ja/Marketplace/Options/Open_web_apps_for_desktop) 版と [Android](https://developer.mozilla.org/ja/Marketplace/Options/Open_web_apps_for_android) 版の Firefox から将来的に削除されることとなりました。

これらの機能は 2011 年に Mozilla Labs で考案され、後にモダンな Web 技術を基盤とした [Firefox OS](https://developer.mozilla.org/ja/Apps/Build/Building_apps_for_Firefox_OS) にとって不可欠な要素となりました。しかしながら、このランタイムは他のプラットフォームでは広く使われたり積極的に開発されることはありませんでした。

これに伴い、[Firefox Marketplace](https://developer.mozilla.org/ja/Marketplace) はデスクトップコンピュータや Android 端末に向けたアプリの配布を中止します。Firefox OS は現時点では影響を受けません。WebKit ベースの iOS 版 Firefox は Open Web Apps に対応していません。
