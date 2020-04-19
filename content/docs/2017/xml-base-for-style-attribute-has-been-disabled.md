---
title: "`xml:base` for `style` attribute has been disabled"
date: "2017-03-26T02:51:00-04:00"
categories: ["css", "misc"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349024"
      title: "Bug 1349024 - Turn off xml:base for style attribute by default on aurora and nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1350521"
      title: "Bug 1350521 - Turn off xml:base for style attribute by default for all channels"
    - url: "https://groups.google.com/d/topic/mozilla.compatibility/z2syZhkI1-U/discussion"
      title: "Intent to Deprecate: xml:base for CSS style attributes"
---
The [`xml:base`](https://www.w3.org/TR/xmlbase/) support for the CSS `style` attribute, as seen below, has been disabled by default with Firefox 55. Given that the `xml:base` attribute [deprecated since Firefox 53](https://www.fxsitecompat.dev/en-CA/docs/2017/xml-base-attribute-has-been-deprecated/) is not supported by any other browsers, the compatibility risk should be very low.

```html
<div xml:base="https://example.com/"
     style="background:url(picture.jpg)"></div>
```

**Update**: The attribute support has been completely removed with [Firefox 66](https://www.fxsitecompat.dev/en-CA/docs/2018/xml-base-attribute-is-no-longer-supported/).
