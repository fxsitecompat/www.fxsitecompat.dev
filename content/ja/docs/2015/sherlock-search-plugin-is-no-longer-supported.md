---
title: "Sherlock 検索プラグイン対応が打ち切られました"
date: "2015-09-23T16:29:00-04:00"
categories: ["misc"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862137": "Bug 862137 - stop supporting Sherlock search engines"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862148": "Bug 862148 - stop supporting installation of Sherlock plugins from the web"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862147": "Bug 862147 - drop support for window.sidebar"
---
[Firefox 24 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2013/support-for-sherlock-search-plug-ins-has-been-deprecated/) 旧来の Sherlock 検索プラグイン形式への対応が Firefox 44 で廃止されました。Web ページから Sherlock プラグインをインストールできるようにしていた [`window.sidebar.addSearchEngine`](https://developer.mozilla.org/ja/docs/Adding_search_engines_from_web_pages#Installing_Sherlock_plugins) メソッドは Web コンソールに警告を残すだけとなりました。代わりに [`window.external.AddSearchProvider`](https://developer.mozilla.org/ja/docs/Adding_search_engines_from_web_pages#Installing_OpenSearch_plugins) メソッドを使って [OpenSearch プラグイン](https://developer.mozilla.org/ja/docs/Creating_OpenSearch_plugins_for_Firefox) を提供できます。

なお、`window.sidebar.addPanel` メソッドを通じたサイドバーパネルのインストール対応は、[Firefox 23 で既に削除されています](https://www.fxsitecompat.com/ja/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/)。非標準の [`window.sidebar`](https://developer.mozilla.org/ja/docs/Web/API/Window/sidebar) オブジェクトは [将来的に完全に削除されます](https://www.fxsitecompat.com/ja/docs/2015/window-sidebar-will-be-removed/) が、まだ様々なサイトでブラウザ判別に使われているようです。今後このオブジェクトを使用することは避けてください。
