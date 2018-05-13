---
title: "`negotiationneeded` イベントが初回オファー前に抑制されなくなりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["audio-video"]
tags: []
versions: ["40"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1149838"
      title: "Bug 1149838 - We should not suppress negotiationneeded before the first offer/answer exchange"
---
[`negotiationneeded`](https://developer.mozilla.org/docs/Web/Reference/Events/negotiationneeded) イベントが初回オファー (応答交換) 前にも正しく実行されるようになりました。このイベントが再交渉時にのみ呼び出されることを想定している場合は、予期せぬ問題を防ぐためコードを見直してください。
