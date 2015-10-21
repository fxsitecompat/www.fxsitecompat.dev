---
title: "SVG favicon is supported; be careful with the order of `<link>`s"
date: "2015-06-13T15:20:46-04:00"
categories: ["html"]
tags: []
versions: ["41"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=366324": "Bug 366324 - SVG site icons (favicons, shortcut icons) support"
---
Firefox 41 has added the long-awaited support for [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) format site icons (favicons). This works fine, but you have to be careful with the order of the [`<link>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link) elements for your favicon. Some popular sites, including [*Flickr*](https://bugzilla.mozilla.org/show_bug.cgi?id=1181681), [*Pinterest*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174568), [*Twitter*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174552) and [*Yelp*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174548), are known to be showing a black SVG icon on Firefox 41, which is for Safari 9's Pinned Tabs, instead of an intended, normal colored favicon. This conflict is occurring because those sites are putting the black icon *after* the other icons, and Firefox uses the last icon specified in the HTML source. The workaround here is, obviously, putting a black SVG icon for Safari *before* other icons, as [recommended by Apple](https://developer.apple.com/library/safari/releasenotes/General/WhatsNewInSafari/Articles/Safari_9.html#//apple_ref/doc/uid/TP40014305-CH9-SW20).
