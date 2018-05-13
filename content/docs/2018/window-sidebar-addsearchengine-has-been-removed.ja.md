---
title: "`window.sidebar.addSearchEngine()` が削除されました"
date: "2018-01-06T03:47:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862147"
      title: "Bug 862147 - remove window.external.addSearchEngine"
---
非標準の `window.sidebar.addSearchEngine` メソッドとそのエイリアスである `window.external.addSearchEngine` は Firefox 59 で削除されました。旧式 Sherlock 検索プラグインのインストール機能は既に [Firefox 44 で削除されており](https://www.fxsitecompat.com/ja/docs/2015/sherlock-search-plug-ins-are-no-longer-supported/)、一方で [OpenSearch プラグイン](https://developer.mozilla.org/docs/Web/OpenSearch) は引き続き Internet Explorer 由来の `window.external.AddSearchProvider` メソッドを使ってインストールできます。

[`window.sidebar`](https://developer.mozilla.org/docs/Web/API/Window/sidebar) オブジェクトはもはや何の役にも立たないため、これも [将来的に削除されます](https://www.fxsitecompat.com/ja/docs/2015/window-sidebar-will-be-removed/)。
