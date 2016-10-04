---
title: "Sherlock 検索プラグイン対応が打ち切られました"
date: "2015-09-23T16:29:00-04:00"
categories: ["misc"]
tags: []
versions: ["44"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862137"
      title: "Bug 862137 - stop supporting Sherlock search engines"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862148"
      title: "Bug 862148 - stop supporting installation of Sherlock plugins from the web"
aliases:
    - "/docs/2015/sherlock-search-plugin-is-no-longer-supported/"
---
[Firefox 24 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2013/support-for-sherlock-search-plug-ins-has-been-deprecated/) 旧式 Sherlock 検索プラグイン形式への対応が Firefox 44 で廃止されました。[`window.sidebar.addSearchEngine`](https://developer.mozilla.org/ja/docs/Adding_search_engines_from_web_pages#Installing_Sherlock_plugins) メソッドは、Web コンテンツから Sherlock のインストールが要求された場合、Web コンソールに警告を残すのみとなりました。

`addSearchEngine` メソッドはまだ [OpenSearch プラグイン](https://developer.mozilla.org/ja/docs/Creating_OpenSearch_plugins_for_Firefox) に対応していますが、[`window.sidebar`](https://developer.mozilla.org/ja/docs/Web/API/Window/sidebar) オブジェクトは [将来的に完全に削除されます](https://www.fxsitecompat.com/ja/docs/2015/window-sidebar-will-be-removed/) ので、代わりに [`window.external.AddSearchProvider`](https://developer.mozilla.org/ja/docs/Adding_search_engines_from_web_pages#Installing_OpenSearch_plugins) メソッドを使ってください。
