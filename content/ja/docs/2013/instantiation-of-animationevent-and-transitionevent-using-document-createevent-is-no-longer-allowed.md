---
title: "`Document.createEvent` による `AnimationEvent` と `TransitionEvent` インスタンスの生成が認められなくなりました"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=868751": "Bug 868751 – Remove support for document.createEvent(\"AnimationEvent\"), document.createEvent(\"TransitionEvent\"), AnimationEvent.initAnimationEvent, and TransitionEvent.initTransitionEvent"
---
古い `document.createEvent("AnimationEvent")`、`document.createEvent("TransitionEvent")`、[`AnimationEvent.initAnimationEvent`](https://developer.mozilla.org/ja/docs/Web/API/AnimationEvent#initAnimationEvent)、[`TransitionEvent.initTransitionEvent`](https://developer.mozilla.org/ja/docs/Web/API/TransitionEvent#initTransitionEvent) への対応が打ち切られました。今後は、標準のコンストラクタである [`AnimationEvent()`](https://developer.mozilla.org/ja/docs/Web/API/AnimationEvent.AnimationEvent) and [`TransitionEvent()`](https://developer.mozilla.org/ja/docs/Web/API/TransitionEvent.TransitionEvent) のみ使用できます。
