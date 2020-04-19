---
title: "Instantiation of `AnimationEvent` and `TransitionEvent` using `Document.createEvent()` is no longer allowed"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
releases: ["23", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=868751"
      title: "Bug 868751 – Remove support for document.createEvent(\"AnimationEvent\"), document.createEvent(\"TransitionEvent\"), AnimationEvent.initAnimationEvent, and TransitionEvent.initTransitionEvent"
---
The support for obsolete `document.createEvent("AnimationEvent")`, `document.createEvent("TransitionEvent")`, [`AnimationEvent.initAnimationEvent`](https://developer.mozilla.org/docs/Web/API/AnimationEvent#initAnimationEvent), and [`TransitionEvent.initTransitionEvent`](https://developer.mozilla.org/docs/Web/API/TransitionEvent#initTransitionEvent) has been removed. Only the standard constructors, [`AnimationEvent`](https://developer.mozilla.org/docs/Web/API/AnimationEvent.AnimationEvent) and [`TransitionEvent`](https://developer.mozilla.org/docs/Web/API/TransitionEvent.TransitionEvent) are now allowed.
