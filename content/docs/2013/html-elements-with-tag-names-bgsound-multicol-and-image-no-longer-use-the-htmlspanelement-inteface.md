---
title: "HTML elements with tag names `bgsound`, `multicol`, and `image` no longer use the `HTMLSpanElement` inteface"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844127"
      title: "Bug 844127 – Stop using the HTMLSpanElement interface for bgsound, multicol, image"
---
Previously, creating an HTML element with one of these tag names resulted in an [`HTMLSpanElement`](https://developer.mozilla.org/docs/Web/API/HTMLSpanElement). Now [`<bgsound>`](https://developer.mozilla.org/docs/Web/HTML/Element/bgsound) and [`<multicol>`](https://developer.mozilla.org/docs/Web/HTML/Element/multicol) are [`HTMLUnknownElement`](https://developer.mozilla.org/docs/Web/API/HTMLUnknownElement) and [`<image>`](https://developer.mozilla.org/docs/Web/HTML/Element/image) is [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement), as per spec.
