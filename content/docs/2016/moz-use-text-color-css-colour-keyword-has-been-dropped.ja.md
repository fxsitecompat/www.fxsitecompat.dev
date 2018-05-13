---
title: "`-moz-use-text-color` CSS カラーキーワードが廃止されました"
date: "2016-10-03T17:30:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306214"
      title: "Bug 1306214 - Remove -moz-use-text-color from color properties"
---
[`border-color`](https://developer.mozilla.org/docs/Web/CSS/border-color)、[`outline-color`](https://developer.mozilla.org/docs/Web/CSS/outline-color)、その他いくつかのプロパティに使用可能だった非標準 CSS カラーキーワード `-moz-use-text-color` への対応が削除されました。標準化された [`currentcolor`](https://developer.mozilla.org/docs/Web/CSS/color_value#currentColor_keyword) キーワードを代わりに使用してください。
