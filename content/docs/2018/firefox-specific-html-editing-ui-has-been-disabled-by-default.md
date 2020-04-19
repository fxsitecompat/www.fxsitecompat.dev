---
title: "Firefox-specific HTML editing UI has been disabled by default"
date: "2018-09-22T13:05:00-04:00"
categories: ["html"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1490641"
      title: "Bug 1490641 - Disable all Gecko specific UIs by default in release build"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
The following editing UI features on the [HTML rich-text editor](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content), only implemented in Firefox so far, are now disabled by default starting from Firefox 64, as requested by the W3C Editing Task Force. These are [considered deprecated](https://www.fxsitecompat.dev/en-CA/docs/2018/firefox-specific-html-editing-ui-has-been-deprecated/) and already disabled by default in Firefox Nightly and early Beta/DevEdition as of Firefox 63.

* object resizing on `<img>`, `<table>` and absolute-positioned elements
* inline table editing to add or remove rows and columns
* grabber for absolute-positioned elements

Web developers can still enable these features using the [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) method as below, but remember that the UI is not available in other browsers and will probably be removed from Firefox in the future.

```js
document.execCommand('enableObjectResizing', false, true);
document.execCommand('enableInlineTableEditing', false, true);
document.execCommand('enableAbsolutePositionEditor', false, true);
```
