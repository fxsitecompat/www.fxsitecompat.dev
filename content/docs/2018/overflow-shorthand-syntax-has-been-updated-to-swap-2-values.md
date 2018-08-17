---
title: "`overflow` shorthand syntax has been updated to swap 2 values"
date: "2018-08-17T11:57:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481866"
      title: "Bug 1481866 - swap values of 2-value 'overflow' syntax so block is first and inline is second"
---
Since [Firefox 61](https://bugzilla.mozilla.org/show_bug.cgi?id=1453148), the CSS [`overflow`](https://developer.mozilla.org/docs/Web/CSS/overflow) property is a shorthand accepting both `overflow-x` and `overflow-y`. After a recent discussion in the CSS Working Group, the syntax has been changed to accept new [logical properties](https://developer.mozilla.org/docs/Web/CSS/CSS_Logical_Properties), `overflow-block` and `overflow-inline`, to better support vertical writing modes. Firefox 63 has updated the implementation accordingly.

It means, the 2 x/y values have to be swapped like this:

```css
overflow-x: scroll;
overflow-y: hidden;
/* On Firefox 61 and 62, this is the same as */
overflow: scroll hidden;
/* But on Firefox 63 and later, it will be */
overflow: hidden scroll;
```

Given that the shorthand syntax is still new and only implemented in the latest versions of Firefox and [Google Chrome](https://www.chromestatus.com/feature/5090725653905408) so far, the compatibility risk should be very low, hence the change.

At the time of writing, the `overflow-block` and `overflow-inline` longhand properties are not implemented yet.
