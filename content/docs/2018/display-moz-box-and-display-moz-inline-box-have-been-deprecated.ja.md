---
title: "`display:-moz-box` と `display:-moz-inline-box` が廃止予定となりました"
date: "2018-08-14T21:04:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1477553"
      title: "Bug 1477553 - Hide display: -moz-box and display: -moz-inline-box from content in Nightly / early beta."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C83tct9EPAk/discussion"
      title: "Intent to unship: display: -moz-box and display: -moz-inline-box from content pages."
---
CSS `display` プロパティ用の非標準値、`-moz-box` と `-moz-inline-box` が廃止予定となり、Firefox Nightly と早期 Beta/DevEdition では初期設定により無効化されました。特に大きな問題がなければ、これらの値は近々すべてのチャンネルから削除されます。

なお、`-moz-grid` や `-moz-inline-grid` など `display` プロパティの他の非標準値は既に [Firefox 62 で廃止されています](https://www.fxsitecompat.dev/ja/docs/2018/most-of-non-standard-css-display-values-have-been-dropped/)。

**更新**: これらの値は [Firefox 64 で削除されました](https://www.fxsitecompat.dev/ja/docs/2018/display-moz-box-and-moz-tree-pseudo-elements-have-been-removed/)。
