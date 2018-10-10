---
title: "`display:-moz-box` と `::-moz-tree` 疑似要素が廃止されました"
date: "2018-10-10T07:46:00-04:00"
categories: ["css"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496961"
      title: "Bug 1496961 - Let some XUL unshipping prefs ride the trains."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C83tct9EPAk/discussion"
      title: "Intent to unship: display: -moz-box and display: -moz-inline-box from content pages."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gbzTmE4uvJk/discussion"
      title: "Intent to unship: ::-moz-tree pseudo-elements."
---
[Firefox 63 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2018/display-moz-box-and-display-moz-inline-box-have-been-deprecated/) CSS `display` プロパティ用の非標準値、`-moz-box` と `-moz-inline-box`、また同じく [Firefox 63 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2018/moz-tree-pseudo-elements-have-been-deprecated/) 以下の非標準 CSS 疑似要素が、 Firefox 64 以降ウェブコンテンツから使用できなくなりました。

これらは既に廃止予定となった [XUL](https://developer.mozilla.org/docs/Mozilla/Tech/XUL) で記述されている Firefox のユーザーインターフェイス用に作られたもので、他のどのブラウザーも対応していません。削除に伴う互換性問題の報告も今のところありません。

* `::-moz-tree-cell`
* `::-moz-tree-cell-text`
* `::-moz-tree-checkbox`
* `::-moz-tree-column`
* `::-moz-tree-drop-feedback`
* `::-moz-tree-image`
* `::-moz-tree-indentation`
* `::-moz-tree-line`
* `::-moz-tree-row`
* `::-moz-tree-separator`
* `::-moz-tree-twisty`
