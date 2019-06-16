---
title: "いくつかの `appearance` キーワードが削除されました"
date: "2019-06-15T19:33:00-04:00"
categories: ["css"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1554150"
      title: "Bug 1554150 - Remove -webkit-appearance keywords that are removed in Chromium 75"
---
Firefox 69 以降、`-webkit-appearance` CSS プロパティとそのエイリアスである `-moz-appearance` 向けの一部キーワードがウェブコンテンツから使用できなくなりました。これは Chrome 75 での削除を受けた措置で、以下のキーワードが含まれます。

* `button-bevel`
* `caret`
* `listitem`
* `menulist-text`
* `menulist-textfield`
