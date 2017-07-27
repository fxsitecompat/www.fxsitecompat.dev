---
title: "CSS `position:fixed` now always creates stacking context"
date: "2015-10-03T11:43:00-04:00"
categories: ["css"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1179288"
      title: "Bug 1179288 - change position:fixed so it always creates a stacking context"
---
The CSS specification has been updated to change [`position:fixed`](https://developer.mozilla.org/en-US/docs/Web/CSS/position#Fixed_positioning) so that it now always creates a [stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context) for Web compatibility. While the new behaviour should match Chrome and Safari, pages and apps relying on the previous Firefox rendering may be broken with this change.
