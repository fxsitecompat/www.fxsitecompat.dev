---
title: "`-moz-orient` の初期値が変更されました"
date: "2015-04-27T13:17:23-04:00"
categories: ["css"]
tags: []
versions: ["40"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1028716"
      title: "Bug 1028716 – update values of -moz-orient for <progress> and <meter> to remove \'auto\', and add \'inline\' (new initial value) and \'block\' values with writing-mode support"
---
[`<progress>`](https://developer.mozilla.org/docs/Web/HTML/Element/progress)、[`<meter>`](https://developer.mozilla.org/docs/Web/HTML/Element/meter) 両要素に適用可能な [`-moz-orient`](https://developer.mozilla.org/docs/Web/CSS/-moz-orient) プロパティの実装が最新仕様に合わせて更新され、これらの要素上で [`writing-mode`](https://developer.mozilla.org/docs/Web/CSS/writing-mode) プロパティに対応しました。これまで初期値だった `auto` は削除され、代わりに新たな初期値となる `inline` と `block` が取り得る値として追加されました。
