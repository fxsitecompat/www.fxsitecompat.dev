---
title: "`<script>` with version parameter will no longer be loaded"
date: "2018-02-23T19:19:00-05:00"
categories: ["html", "javascript"]
tags: []
releases: ["59", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867609"
      title: "Bug 867609 - Retire JavaScript versions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867612"
      title: "Bug 867612 - Make sure JavaScript version is not used on the web"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1428745"
      title: "Bug 1428745 - Remove support for version parameter from script loader"
aliases:
    - "/en-CA/docs/2015/javascript-versions-will-be-retired/"
---
Traditionally, Firefox has required an explicit `version` parameter for the `<script>` element's `type` attribute to use the advanced features of JavaScript [1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) and [1.8](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.8).

```html
<script type="application/javascript;version=1.7"></script>
<script type="application/javascript;version=1.8"></script>
```

Starting with Firefox 44, the `let` statement [no longer requires an explicit JavaScript version](https://www.fxsitecompat.dev/en-CA/docs/2015/let-statement-no-longer-requires-explicit-javascript-version/). Meanwhile, the support for [destructuring `for-in`](https://www.fxsitecompat.dev/en-CA/docs/2015/destructuring-for-in-loop-has-been-removed/), [legacy iterators](https://www.fxsitecompat.dev/en-CA/docs/2017/legacy-iterator-protocol-has-been-removed/), [legacy generators](https://www.fxsitecompat.dev/en-CA/docs/2017/legacy-generator-support-has-been-removed/), [array comprehensions](https://www.fxsitecompat.dev/en-CA/docs/2017/array-generator-comprehension-support-has-been-removed/) and [expression closures](https://www.fxsitecompat.dev/en-CA/docs/2017/expression-closure-support-has-been-removed/) added with JavaScript 1.7 and 1.8 has been removed in favour of the standard alternatives.

As part of the standardization efforts, the support for the Firefox-specific JavaScript `version` parameter has also been removed with Firefox 59. It means `<script>` with any `version` parameter will no longer be loaded because those will be treated as scripts of an unknown MIME type like `text/template`. According to Mozilla's telemetry, this change may affect 0.02% of script loading.

If you are serving JavaScript, you can simply omit the `type` attribute which is optional in HTML5 as well as the newer HTML Living Standard, or you should be using one of the [standard JavaScript MIME types](https://mimesniff.spec.whatwg.org/#javascript-mime-type) including `text/javascript` and `application/javascript` without any parameters.
