---
title: "Firefox OS アプリは常にビューポート `<meta>` タグを指定してください"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=845690": "Bug 845690 – Support meta viewport in Firefox OS apps"
---
Firefox 28 を元にした [Firefox OS 1.3](https://developer.mozilla.org/ja/Firefox_OS/Releases/1.3) で、アプリケーション内の [ビューポート `<meta>` タグ](https://developer.mozilla.org/ja/docs/Mozilla/Mobile/Viewport_meta_tag) 対応が追加されました。ビューポートが指定されていないアプリには、既定の `"width=device-width, height=device-height, user-scalable=no"` が適用されます。この実装は後方互換のみを考慮したもので、将来的には削除されます。[Open Web App](https://developer.mozilla.org/ja/Apps/Quickstart/Build/Intro_to_open_web_apps) 開発者には、将来起こりうる問題を防ぐため、ビューポート `<meta>` タグを常に指定するよう推奨します。
