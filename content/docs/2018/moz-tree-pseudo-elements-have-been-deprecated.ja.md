---
title: "`::-moz-tree` 疑似要素が廃止予定となりました"
date: "2018-08-14T21:29:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1480054"
      title: "Bug 1480054 - Don't allow tree pseudos with arguments in content."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gbzTmE4uvJk/discussion"
      title: "Intent to unship: ::-moz-tree pseudo-elements."
---
以下の非標準 CSS 疑似要素が廃止予定となり、Firefox Nightly と早期 Beta/DevEdition では初期設定により無効化されました。特に大きな問題がなければ、これらの疑似要素は近々すべてのチャンネルから削除されます。

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

**更新**: これらの疑似要素は [Firefox 64 で削除されました](https://www.fxsitecompat.com/ja/docs/2018/display-moz-box-and-moz-tree-pseudo-elements-have-been-removed/)。
