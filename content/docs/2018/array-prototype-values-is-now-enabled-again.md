---
title: "`Array.prototype.values()` is now enabled again"
date: "2018-02-11T00:08:00-05:00"
categories: ["javascript"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1420101"
      title: "Bug 1420101 - Array.prototype.values() does not exist"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/s92kdFNjL0U/discussion"
      title: "Intent to ship: Array.prototype.values"
---
Firefox 60 has re-enabled the support for the standard [`Array.prototype.values`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/values) method, which was implemented with Firefox 48 but has been disabled other than on the Nightly channel due to [some compatibility issues](https://www.fxsitecompat.com/en-CA/docs/2016/array-prototype-values-breaks-some-legacy-apps/).

Microsoft Edge and Apple Safari have already shipped the feature. [Google Chrome 66](https://www.chromestatus.com/feature/4755812090118144) coming this April will also enable it again. In order to avoid breakage, please make sure your site doesn't have any arbitrary implementation of the method.
