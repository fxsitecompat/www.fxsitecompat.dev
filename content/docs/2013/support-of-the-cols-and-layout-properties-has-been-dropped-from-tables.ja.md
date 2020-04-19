---
title: "テーブルから `cols`、`layout` 両プロパティの実装が削除されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=835169"
      title: "Bug 835169 – Do we need support for the table[cols] attribute?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=835439"
      title: "Bug 835439 – Remove support for the table[layout] attribute"
---
Firefox は [`<table>`](https://developer.mozilla.org/docs/Web/HTML/Element/table) 要素上で `cols`、`layout` プロパティを受け入れなくなりました。他のどのブラウザーもこれらの無名プロパティに対応していません。
