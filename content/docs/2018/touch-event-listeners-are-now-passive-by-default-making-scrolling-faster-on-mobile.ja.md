---
title: "モバイル上のスクロールを高速化するため、タッチイベントリスナーが標準でパッシブとなりました"
date: "2018-04-25T18:02:00-04:00"
categories: ["dom"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449268"
      title: "Bug 1449268 - Treat document-level touch event listeners as passive. (Chrome scrolling intervention)"
---
Firefox 61 以降、`window`、`document`、`document.body` 上の `touchstart` および `touchmove` イベントリスナーは標準でパッシブ (無抵抗) として扱われます。つまり、[`addEventListener`](https://developer.mozilla.org/docs/Web/API/EventTarget/addEventListener) の `passive` オプションを明示的に `false` に設定しない限り、それらのイベントは [`preventDefault()`](https://developer.mozilla.org/docs/Web/API/Event/preventDefault) を使ってキャンセルできなくなります。

このスクロール介入は、[Google Developers サイトの記事](https://developers.google.com/web/updates/2017/01/scrolling-intervention) で説明されている通り、モバイル端末上でのスクロールパフォーマンス向上を目的としたものです。2017 年 1 月公開の Chrome 56 が既にこの新しい挙動を採用していることから、互換性リスクは低いはずです。

**更新**: [Firefox 70](https://www.fxsitecompat.dev/ja/docs/2019/ontouchstart-ontouchmove-event-handlers-are-now-passive-by-default/) で同様の変更が `ontouchstart` と `ontouchmove` イベントハンドラーに対して行われました。
