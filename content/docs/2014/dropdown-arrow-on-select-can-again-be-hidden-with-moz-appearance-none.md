---
title: "Dropdown arrow on `<select>` can again be hidden with `-moz-appearance:none`"
date: "2014-10-17T22:50:44-04:00"
categories: ["css"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=649849"
      title: "Bug 649849 – Make -moz-appearance:none on a combobox remove the dropdown button"
---
Since a wrong `padding` implementation on the [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) element was [fixed with Firefox 30](https://www.fxsitecompat.dev/en-CA/docs/2014/incorrect-padding-implementation-on-select-has-been-fixed/), a hack to hide the combobox's dropdown arrow, using [`-moz-appearance`](https://developer.mozilla.org/docs/Web/CSS/-moz-appearance)`:none` in combination with the [`text-indent`](https://developer.mozilla.org/docs/Web/CSS/text-indent) and [`text-overflow`](https://developer.mozilla.org/docs/Web/CSS/text-overflow) properties, has stopped working. This non-standard behaviour has been restored with Firefox 35 as many developers wanted to have control over the combobox style. Now `-moz-appearance:none` can simply be used to hide the dropdown arrow as before, just like `-webkit-appearance:none`.
