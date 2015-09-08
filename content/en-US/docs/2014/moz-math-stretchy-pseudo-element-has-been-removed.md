---
title: "`::-moz-math-stretchy` pseudo-element has been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["css"]
tags: []
versions: "31"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1000879": "Bug 1000879 – Remove the ::-moz-math-stretchy pseudo-element."
---
The support for the non-standard `::-moz-math-stretchy` pseudo-element, which allowed authors to specify a [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) to use for stretchy operators, has been removed. A [math font](https://developer.mozilla.org/en-US/docs/Mozilla/MathML_Project/Fonts) specified on a [`<math>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/math) element is now inherited to the child nodes.
