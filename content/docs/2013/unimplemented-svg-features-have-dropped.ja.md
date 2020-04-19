---
title: "未実装の SVG 機能が削除されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["svg"]
tags: []
versions: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=824218"
      title: "Bug 824218 – Remove unimplemented SVG features"
---
未実装の SVG 機能が、単に `NOT_IMPLEMENTED` エラーを返す代わりに削除されました。これらの機能には [`SVGSVGElement`](https://developer.mozilla.org/docs/Web/API/SVGSVGElement) の `viewport`、`currentView` プロパティが含まれます。
