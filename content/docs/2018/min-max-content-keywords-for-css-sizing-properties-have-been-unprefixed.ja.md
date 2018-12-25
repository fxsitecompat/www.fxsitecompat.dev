---
title: "CSS サイズ関連プロパティ用の `min`/`max-content` キーワードの接頭辞が外れました"
date: "2018-12-25T00:32:00-05:00"
categories: ["css"]
tags: []
versions: ["66"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1322780"
      title: "Bug 1322780 - Unprefix min-content and max-content keywords"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vyCAurCC2DI/discussion"
      title: "Intent to ship: unprefixed max-content and min-content for css sizing properties"
---
`width`、`height` や `flex-basis` といった CSS サイズ関連プロパティに使用可能な `min-content`、`max-content` 両キーワードが Firefox 66 以降接頭辞なしで使用可能となりました。Google Chrome はバージョン 46 以降接頭辞なしのキーワードに対応しています。

接頭辞付きのバージョンである `-moz-min-content` と `-moz-max-content` は引き続きエイリアスとして対応が行われますが、廃止予定はまだ発表されていません。
