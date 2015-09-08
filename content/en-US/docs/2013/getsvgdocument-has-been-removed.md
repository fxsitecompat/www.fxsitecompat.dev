---
title: "`GetSVGDocument` has been removed"
date: "2013-05-19T07:35:00-04:00"
categories: ["svg"]
tags: []
versions: "24"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=881128": "Bug 881128 – Remove nsIDOMGetSVGDocument"
---
The `GetSVGDocument` interface has been removed. No other browsers are exposing it on the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) object. The [`getSVGDocument`](https://developer.mozilla.org/en-US/docs/Web/SVG/Scripting#Inter-document_scripting.3A_referencing_embedded_SVG) method on the [`<embed>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed), [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) and [`<object>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object) elements is still available.
