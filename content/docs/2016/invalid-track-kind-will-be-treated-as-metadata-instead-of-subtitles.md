---
title: "Invalid `<track kind>` will be treated as `metadata` instead of `subtitles`"
date: "2016-05-10T12:24:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269712"
      title: "Bug 1269712 - A <track kind=invalid> should behave like metadata, not subtitles"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/42-W463M4Ig/discussion"
      title: "Intent to ship: invalid <track kind> values behave like \"metadata\", not \"subtitles\""
---
Previously, invalid values specified for the `kind` attribute on the [`<track>`](https://developer.mozilla.org/docs/Web/HTML/Element/track) element were treated as `subtitles`, the default value. In order to introduce new kinds in the future without breaking the backward compatibility, any invalid values now behave like `metadata` that won't accidentally visible to the user. According to Opera's research, only 0.001% of pages will be affected of this change.
