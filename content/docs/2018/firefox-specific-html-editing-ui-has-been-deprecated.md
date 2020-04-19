---
title: "Firefox-specific HTML editing UI has been deprecated"
date: "2018-08-17T13:28:00-04:00"
categories: ["html"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449564"
      title: "Bug 1449564 - Disable table/image resizers in default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
The following editing UI features on the [HTML rich-text editor](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content), only implemented in Firefox so far, are now considered deprecated and disabled by default in Firefox Nightly and early Beta/DevEdition as of Firefox 63. Assuming no major issues arise, these features will be disabled by default in all the channels with Firefox 64.

* object resizing on `<img>`, `<table>` and absolute-positioned elements
* inline table editing to add or remove rows and columns
* grabber for absolute-positioned elements

Web developers can still enable these features using the [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) method as below, but remember that the UI is not available in other browsers and will probably be removed from Firefox in the future.

```js
document.execCommand('enableObjectResizing', false, true);
document.execCommand('enableInlineTableEditing', false, true);
document.execCommand('enableAbsolutePositionEditor', false, true);
```

**Update**: The initial draft of this article was saying that these features will be removed with Firefox 64. However, the current plan is only to be disabled by default with the upcoming release. The content has been corrected accordingly.

**Update 2**: Starting with [Firefox 64](https://www.fxsitecompat.dev/en-CA/docs/2018/firefox-specific-html-editing-ui-has-been-disabled-by-default/), these features are disabled by default on all the Firefox channels as planned.
