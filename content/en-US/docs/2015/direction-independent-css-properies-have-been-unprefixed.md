---
title: "Direction-independent CSS properies have been unprefixed"
date: "2015-09-24T14:26:00-04:00"
categories: ["css"]
tags: []
versions: ["41"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138384": "Bug 1138384 - enable CSS writing-mode support in release channels"
---
As a part of the CSS3 Writing Modes implementation, various direction-independent CSS properties for `margin`, `border` and `padding`, that could be used to easier support <abbr title="Right-to-Left">RTL</abbr> languages like Arabic, have been unprefixed. Since the unprefixed properties are not just without `-moz-` as the table below shows, you should be careful when using these ones.

| Prefixed properties       | Unprefixed properties                                                                                     |
| ------------------------- | --------------------------------------------------------------------------------------------------------- |
| `-moz-margin-start`       | [`margin-inline-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-inline-start)             |
| `-moz-margin-end`         | [`margin-inline-end`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-inline-end)                 |
| `-moz-border-start`       | [`border-inline-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-start)             |
| `-moz-border-start-width` | [`border-inline-start-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-start-width) |
| `-moz-border-start-style` | [`border-inline-start-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-start-style) |
| `-moz-border-start-color` | [`border-inline-start-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-start-color) |
| `-moz-border-end`         | [`border-inline-end`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-end)                 |
| `-moz-border-end-width`   | [`border-inline-end-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-end-width)     |
| `-moz-border-end-style`   | [`border-inline-end-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-end-style)     |
| `-moz-border-end-color`   | [`border-inline-end-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-inline-end-color)     |
| `-moz-padding-start`      | [`padding-inline-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-inline-start)           |
| `-moz-padding-end`        | [`padding-inline-end`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-inline-start)             |

Due to a bug, Firefox 41 still shows the prefixed properties on the Page Inspector, [`CSSRule.cssText`](https://developer.mozilla.org/en-US/docs/Web/API/CSSRule/cssText) and other APIs. This issue has been [fixed with Firefox 42](https://www.fxsitecompat.com/en-US/docs/2015/cssrule-csstext-now-returns-unprefixed-writing-mode-aware-properties/).

The support for the prefixed properties will be removed in the future.
