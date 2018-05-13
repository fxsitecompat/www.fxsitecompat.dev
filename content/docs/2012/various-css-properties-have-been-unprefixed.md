---
title: "Various CSS properties have been unprefixed"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=762302"
      title: "Bug 762302 – [css3-animations] unprefix CSS Animation properties and @keyframes rule"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=762303"
      title: "Bug 762303 – [css3-transitions] unprefix CSS Transition properties"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=745523"
      title: "Bug 745523 – [css3-transforms] Unprefix transforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=752187"
      title: "Bug 752187 – Drop prefix for gradients"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=771678"
      title: "Bug 771678 – [css3-values] unprefix calc()"
---
All properties of CSS [Animations](https://developer.mozilla.org/docs/Web/CSS/CSS_Animations), [Transitions](https://developer.mozilla.org/docs/Web/CSS/CSS_Transitions) and [Transforms](https://developer.mozilla.org/docs/Web/CSS/CSS_Transforms) are now available without the `-moz-` vendor prefix. The [`@keyframes`](https://developer.mozilla.org/docs/Web/CSS/@keyframes) rule, the [`calc`](https://developer.mozilla.org/docs/Web/CSS/calc) function and [gradient](https://developer.mozilla.org/docs/Web/CSS/CSS_Images/Using_CSS_gradients) functions have also been unprefixed. Gradients require a special attention because the [syntax varies](https://hacks.mozilla.org/2012/07/aurora-16-is-out/) with and without the prefix.

Whenever you use a prefixed property or function, make sure you have the unprefixed one as well for forward compatibility. Stylesheets lacking in such consideration could become unapplied in the future.
