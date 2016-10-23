---
title: "デスクトップ版および Android 版 Firefox から Web App Runtime が削除されました"
date: "2016-02-09T08:19:00-05:00"
categories: ["misc"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1235869"
      title: "Bug 1235869 - Remove support for WebRT"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1238079"
      title: "Bug 1238079 - disable and remove runtime"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1238576"
      title: "Bug 1238576 - Stop exposing navigator.mozApps on desktop and Android"
    - url: "https://groups.google.com/d/topic/firefox-dev/WV2XkVN3sWQ/discussion"
      title: "firefox-dev: disabling the desktop/Android Web Runtimes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.webapps/PUm4nx4A3X8/discussion"
      title: "mozilla.dev.webapps: alternatives to desktop/Android web runtimes"
aliases:
    - "/docs/2016/web-app-runtime-will-be-removed-from-firefox-for-desktop-and-android/"
---
ウェブアプリケーションをネイティブアプリケーションのようにユーザーの端末へインストールし実行することを可能にしていた、非標準の [Open Web Apps JavaScript API](https://developer.mozilla.org/ja/Apps/Build/JavaScript_API) と [Web App Runtime](https://developer.mozilla.org/ja/Apps/Build/Architecture) が、[デスクトップ](https://developer.mozilla.org/ja/Marketplace/Options/Open_web_apps_for_desktop) 版と [Android](https://developer.mozilla.org/ja/Marketplace/Options/Open_web_apps_for_android) 版の Firefox 47 から削除されました。

これらの機能は 2011 年に Mozilla Labs で考案され、後にモダンなウェブ技術を基盤とした [Firefox OS](https://developer.mozilla.org/ja/Apps/Build/Building_apps_for_Firefox_OS) にとって不可欠な要素となりました。しかしながら、このランタイムは他のプラットフォームでは広く使われたり積極的に開発されることはありませんでした。

これに伴い、[Firefox Marketplace](https://developer.mozilla.org/ja/Marketplace) はデスクトップコンピューターや Android 端末に向けたアプリの配布を中止します。Firefox OS は現時点では影響を受けません。WebKit ベースの iOS 版 Firefox は Open Web Apps に対応していません。
