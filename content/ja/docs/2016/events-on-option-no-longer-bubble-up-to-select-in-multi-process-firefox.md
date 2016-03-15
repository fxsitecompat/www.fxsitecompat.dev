---
title: "マルチプロセス Firefox で `<option>` 上のイベントが `<select>` まで浮上しなくなりました"
date: "2016-02-16T09:23:00-05:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1090602"
      title: "Bug 1090602 - [e10s] <option> events do not bubble up through parent <select>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/9Li1-qBaM88/discussion"
      title: "mozilla.dev.platform: Proposal to converge with Chromium / Blink for not firing events on <option>’s from <select> dropdowns"
---
Firefox では、[`<option>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/option) 要素上で発動された [キーボードイベント](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent) や [マウスイベント](https://developer.mozilla.org/ja/docs/Web/API/MouseEvent) は、その親の [`<select>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/select) 要素まで浮上します。一方 Google Chrome ではそうした浮上は見られません。この挙動は実際のところ、詳細がまだ HTML 仕様で規定されていなことから、[ブラウザによって異なります](https://bugzilla.mozilla.org/show_bug.cgi?id=1090602#c27)。

Web 互換性の向上と技術的な理由から、`<select>` 要素がドロップダウンリストとして表示されており、なおかつ [Firefox がマルチプロセスモードで実行されている](https://www.fxsitecompat.com/en-CA/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/) 場合、これらのイベントは浮上しません。`<select>` がインラインで表示されている場合、つまり `multiple` 属性が指定されているか、`size` 属性が指定され `1` よりも大きな値となっている場合、挙動はこれまでと変わりません。
