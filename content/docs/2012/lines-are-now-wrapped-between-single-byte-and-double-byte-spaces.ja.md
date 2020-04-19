---
title: "半角空白と全角空白の間で行が折り返されるようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["misc"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=765166"
      title: "Bug 765166 – IDEOGRAPHIC SPACE (U+3000) should cause line break after a white space"
---
これは、ある日本語のサイトについて「Firefox のみページレイアウトが崩れる」と指摘があった問題です。他のブラウザーと同様に、半角空白 (`U+0020`) と全角空白 (`U+3000`) の間で期待通りに行が折り返されるよう修正が行われました。
