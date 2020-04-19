---
title: "Lines are now wrapped between single-byte and double-byte spaces"
date: "2012-10-09T06:00:00-04:00"
categories: ["misc"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=765166"
      title: "Bug 765166 – IDEOGRAPHIC SPACE (U+3000) should cause line break after a white space"
---
This was an issue on a Japanese site where the page layout was broken only on Firefox. It's now fixed so lines are wrapped as expected between a single-byte space (`U+0020`) and a double-byte space (`U+3000`) like other browsers.
