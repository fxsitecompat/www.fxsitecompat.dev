---
title: "`ontouchstart`、`ontouchmove` イベントハンドラーが標準でパッシブとなりました"
date: "2019-09-04T23:51:00-04:00"
categories: ["dom"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574223"
      title: "Bug 1574223 - Consider treating document level ontouchmove as passive"
---
Firefox 70 以降、`window`、`document`、`document.documentElement`、`document.body` 上の `ontouchstart` あるいは `ontouchmove` プロパティで設定されたイベントハンドラーは標準でパッシブ (無抵抗) として扱われます。つまり、ハンドラーメソッド内で `preventDefault()` を使ってそのイベントをキャンセルすることができなくなります。

[Firefox 61](https://www.fxsitecompat.dev/ja/docs/2018/touch-event-listeners-are-now-passive-by-default-making-scrolling-faster-on-mobile/) で既に同様の変更が `addEventListener()` を使って設定されたイベントリスナーに対して行われており、これはそのモバイル上でのスクロールパフォーマンス向上の見過ごされていたケースでした。
