---
title: "Default style of `<abbr>`/`<acronym>` has been changed"
date: "2015-04-27T13:17:23-04:00"
categories: ["css"]
tags: []
versions: ["40"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1157083"
      title: "Bug 1157083 - It might be better to use CSS3 text-decoration for the UA stylesheet of <abbr> and <acronym> rather than border-bottom"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6FETMqsuQhk/discussion"
      title: "mozilla.dev.platform: Intent to change UA stylesheet of <abbr> and <acronym> (using border-bottom -> CSS 3 text-decoration)"
---
The Firefox user agent stylesheet has been updated to use the CSS3 [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) property for the [`<abbr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr) and [`<acronym>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym) elements. Specifically, `border-block-end: dotted 1px` has been replaced with `text-decoration: dotted underline`. If you are styling one of those elements, you may want to make sure that your own style is not conflicting with the UA stylesheet. Note that Google Chrome is still using [`border-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom) instead of `text-decoration`, so you still have to use both properties to style those as intended.

Currently, [*Bootstrap*](https://github.com/twbs/bootstrap/issues/16574) and [*Normalize.css*](https://github.com/necolas/normalize.css/pull/451) are known to be affected by this change. Those developers are working on the workaround, and the users of the libraries may have to update the code.
