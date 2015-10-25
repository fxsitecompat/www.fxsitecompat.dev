---
title: "Sherlock 検索プラグイン対応が廃止予定となりました"
date: "2013-05-19T07:35:00-04:00"
categories: ["misc"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862143": "Bug 877135 – stop loading Sherlock files from disk"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862137": "Bug 862137 – stop supporting Sherlock search engines"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862148": "Bug 862148 – stop supporting installation of Sherlock plugins from the web"
---
Firefox 24 以降、Sherlock 形式の検索エンジンプラグインがローカルファイルから読み込まれなくなりました。Sherlock 対応と、Web ページから Sherlock プラグインのインストールを可能とする `window.sidebar.addSearchEngine` 関数も、非標準 [`window.sidebar`](https://developer.mozilla.org/ja/docs/Web/API/window.sidebar) API の削除に伴って近い将来削除される見込みです。Web サイト運営者は代わりに [OpenSearch プラグインを提供](https://developer.mozilla.org/ja/docs/Creating_OpenSearch_plugins_for_Firefox) してください。

**更新**: Sherlock 対応は [Firefox 44 で削除されました](https://www.fxsitecompat.com/ja/docs/2015/sherlock-search-plugin-is-no-longer-supported/)。
