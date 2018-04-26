---
title: "`position:relative` on table elements is no longer ignored"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=63895"
      title: "Bug 63895 – positioned internal table elements not abs pos containing block"
---
Previously, `position:relative` specified on table elements was ignored on Firefox because the effect was "undefined" in the CSS2 spec, while it worked as "expected" on other browsers. If you'd like to have an absolutely-positoned element in the table cell, a common workaround was putting an extra, relatively-positioned [`<div>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) element beneath [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td).

The Firefox implementation has been changed to accept `position:relative` as the effect has been defined in the CSS3 spec. You may want to keep the workaround above for the backward compatibility at least until Firefox 24 [<abbr title="Extended Support Release">ESR</abbr>](https://www.mozilla.org/en-US/firefox/organizations/) reaches the end of support in <time datetime="2014-10">October 2014</time>.

This change may potentially break pages that apply `position:relative` to table elements other than [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) while the author expects nothing to happen. The [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) will warn such a case to make tracking down the issue easy.
