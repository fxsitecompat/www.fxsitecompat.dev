---
title: "Microdata API has been removed"
date: "2016-05-24T09:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909633"
      title: "Bug 909633 - Remove HTML Microdata API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=802548"
      title: "Bug 802548 - HTML5 microdata gives special meaning to itemId breaking some web content"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/tgXlkRhF6wo/discussion"
      title: "Intent to unship: HTML microdata API"
aliases:
    - "/en-CA/docs/2015/microdata-api-will-be-removed-by-the-end-of-2015/"
---
The [Microdata DOM API](https://developer.mozilla.org/docs/Web/API/Microdata_DOM_API) was implemented with Firefox 16 but later removed from the HTML5 spec, and no other browsers are implementing it so far. The support for the obsolete API has been removed with Firefox 49 in hope of avoiding further [site compatibility issues](https://www.fxsitecompat.com/en-CA/docs/2012/microdata-api-has-added-new-properties-to-elements/) mainly due to the `itemId` property. For upward compatibility, Web developers are still encouraged to use the [`dataset`](https://developer.mozilla.org/docs/Web/API/HTMLElement/dataset) property instead of any arbitrary properties.

Note that [Microdata](https://developer.mozilla.org/docs/Web/HTML/Microdata) itself is still a part of the [HTML Living Standard](https://html.spec.whatwg.org/multipage/microdata.html) (but not in W3C HTML) and widely used for structured data markup especially with [Schema.org](https://schema.org/) vocabularies. Firefox has just removed the DOM API support.
