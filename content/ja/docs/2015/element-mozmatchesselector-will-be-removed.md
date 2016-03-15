---
title: "`Element.mozMatchesSelector` が削除されます"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119718"
      title: "Bug 1119718 - Remove mozMatchesSelector"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1216193"
      title: "Bug 1216193 - Implement webkitMatchesSelector"
---
`Element.mozMatchesSelector` メソッドが、標準の [`Element.matches`](https://developer.mozilla.org/ja/docs/Web/API/Element/matches) メソッドに置き換えられる形でまもなく削除されます。Web 相互運用性のため標準化された `webkitMatchesSelector` も Firefox 44 で実装されていますが、接頭辞なしのメソッドが常に推奨されます。
