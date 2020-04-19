---
title: "`@-moz-document url-prefix()` CSS hack will no longer work"
date: "2018-06-05T17:57:00-04:00"
categories: ["css", "privacy-security"]
tags: []
releases: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449753"
      title: "Bug 1449753 - Turn off layout.css.moz-document.url-prefix-hack.enabled by default."
---
The [`@-moz-document`](https://developer.mozilla.org/docs/Web/CSS/@document) CSS at-rule has been [disabled with Firefox 61](https://www.fxsitecompat.dev/en-CA/docs/2018/moz-document-support-has-been-dropped-except-for-empty-url-prefix/) to mitigate the risk of CSS injection attacks, but the empty `url-prefix` function is still being parsed because it's known to be used as a [CSS hack targeting Firefox](https://css-tricks.com/snippets/css/css-hacks-targeting-firefox/).

```css
/* This only works with Firefox */
@-moz-document url-prefix() {
  #prices td {
    height: 100%;
  }
}
```

Given the security concerns, the remaining support will also be dropped in the near future anyway once major compatibility issues are solved. If you're using this hack to work around a specific layout bug in Firefox, please [report the issue to Bugzilla](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Layout&blocked=1449753) or [let us know](https://www.fxsitecompat.dev/en-CA/contribute/).
