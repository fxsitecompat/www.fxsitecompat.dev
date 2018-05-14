---
title: "イメージマップがインライン要素として表示されるようになりました"
date: "2012-12-03T03:50:54-05:00"
categories: ["css"]
tags: []
versions: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=607267"
      title: "Bug 607267 – Image maps are display:block, but the HTML spec says they should be inline"
---
イメージマップ ([`map`](https://developer.mozilla.org/docs/HTML/Element/map) 要素) は従来、Firefox の Standards Compliant (標準準拠) モードでは [ブロック要素](https://developer.mozilla.org/docs/HTML/Block-level_elements) として表示されていましたが、[HTML5](https://developer.mozilla.org/docs/HTML/HTML5) の仕様に合わせて [インライン要素](https://developer.mozilla.org/docs/HTML/Inline_elements) に変更されました。[Quirks (後方互換) モード](https://developer.mozilla.org/docs/Mozilla_Quirks_Mode_Behavior) や他のブラウザーでは元々インライン要素として表示されていました。従来通りブロック要素として表示したいときは、スタイルシートに `map { display: block; }` と記述する必要があります。
