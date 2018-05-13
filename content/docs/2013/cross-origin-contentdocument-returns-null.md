---
title: "Cross-origin `contentDocument` returns `null`"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=829872"
      title: "Bug 829872 – Consider returning null from contentDocument getters when the caller does not subsume the document"
---
The `contentDocument` property on frames now returns [`null`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/null) if the caller doesn't subsume the document. This change affects the `contentDocument` property on the [`<frame>`](https://developer.mozilla.org/docs/Web/HTML/Element/frame), [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) and [`<object>`](https://developer.mozilla.org/docs/Web/HTML/Element/object) elements as well as the [`getSVGDocument`](https://developer.mozilla.org/docs/Web/SVG/Scripting#Inter-document_scripting.3A_referencing_embedded_SVG) method on the [`<embed>`](https://developer.mozilla.org/docs/Web/HTML/Element/embed), [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) and [`<object>`](https://developer.mozilla.org/docs/Web/HTML/Element/object) elements.
