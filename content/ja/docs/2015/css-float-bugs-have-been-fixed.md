---
title: "CSS `float` 関連のバグが修正されました"
date: "2015-09-23T07:14:00-04:00"
categories: ["css"]
tags: []
versions: ["42"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=451791"
      title: "Bug 451791 - CSS margin-top collapses across cleared element inside previous sibling and out top of previous sibling (works in Safari, but Firefox has a bug)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=478834"
      title: "Bug 478834 - table (or other BFC) following float doesn't clear it even if it can't fit next to it, when lined up at their tops"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=538194"
      title: "Bug 538194 - non-floated block formatting context only checks top edge for overlap with floats rather than entire height"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1196255"
      title: "Bug 1196255 - tabzilla invisible on mobile view of /privacy/tips/"
---
CSS の [`float`](https://developer.mozilla.org/ja/docs/Web/CSS/float) 処理に関して長年にわたって存在していたいくつかの問題が Firefox 42 で修正されました。

最初のバグでは、`margin-top` と `margin-bottom` プロパティが特定の状況で `float` プロパティとともに使われた場合に誤って適用されることがありました。2 つ目のバグでは、フロートされた要素に続く `<table>` が適切にクリアされず、結果としてコンテンツの重なり合いが発生していました。3 つ目のバグでは、異なる幅を持つ 2 つのフロートされた要素がそれに続く要素の誤配置につながり、これもコンテンツの重なり合いを発生させていました。

これらの変更は仕様や他のブラウザの挙動に合わせた形になるはずですが、Firefox の従来の挙動に依存している一部のページでレイアウトが崩れる可能性があります。実際、Mozilla 自身のサイトが影響を受けています。
