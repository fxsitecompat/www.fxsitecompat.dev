---
title: "Blink effect with `text-decoration:blink` has been dropped"
date: "2013-04-06T04:52:59-04:00"
categories: ["css"]
tags: []
versions: ["23"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=857820"
      title: "Bug 857820 – Drop only blink effect from text-decoration: blink; and completely remove <blink> element"
---
Firefox previously supported the Netscape-derived blink effect with the `blink` keyword for the CSS [`text-decoration`](https://developer.mozilla.org/docs/Web/CSS/text-decoration) property as well as the HTML [`<blink>`](https://developer.mozilla.org/docs/Web/HTML/Element/blink) element and the DOM [`String.blink`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/blink) method. Starting with Firefox 23, the blink effect no longer works. While `text-decoration:blink` continues to be supported by the CSS parser and the DOM APIs, the HTML parser has dropped the [`<blink>`](https://developer.mozilla.org/docs/Web/HTML/Element/blink) element support, thus the element will be treated as an unknown element. Internet Explorer, Chrome and Safari haven't supported the effect. Opera may also drop the support once it switches to the Blink rendering engine.
