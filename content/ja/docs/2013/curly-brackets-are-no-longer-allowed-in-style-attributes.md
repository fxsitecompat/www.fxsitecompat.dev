---
title: "`style` 属性内の中括弧が許容されなくなりました"
date: "2013-10-08T20:15:35-04:00"
categories: ["css"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=915053": "Bug 915053 – remove quirk allowing {} around style attribute"
---
従来、Firefox の [Quirks (後方互換) モード](https://developer.mozilla.org/ja/docs/Mozilla_Quirks_Mode_Behavior) では、CSS パーサは `<div style="{ color: blue; }">` のような `style` 属性の内容を囲む中括弧を許容していました。相互運用性を高めるため、この挙動は Firefox 27 で廃止されました。
