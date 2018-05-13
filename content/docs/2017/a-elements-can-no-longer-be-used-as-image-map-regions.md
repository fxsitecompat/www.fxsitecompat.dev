---
title: "`<a>` elements can no longer be used as image map regions"
date: "2017-11-09T09:12:00-05:00"
categories: ["html"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317937"
      title: "Bug 1317937 - Stop supporting <a> as <area> in image maps (Assertion failure: !aContent->GetPrimaryFrame() || aState.mCreatingExtraFrames || aContent->NodeInfo()->NameAtom() == nsGkAtoms::area, at nsCSSFrameConstructor.cpp:5687)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JUB5K-sz6ek/discussion"
      title: "Intent to unship: <a> as <area> in image maps"
---
In HTML 4, [`<a>`](https://developer.mozilla.org/docs/Web/HTML/Element/a) elements could be used as the hotspot regions on a [`<map>`](https://developer.mozilla.org/docs/Web/HTML/Element/map), like [`<area>`](https://developer.mozilla.org/docs/Web/HTML/Element/area) elements, in combination with the `coords` and `shape` attributes. Firefox 58 has dropped the support for this functionality because it was implemented by no other browsers and also removed from the HTML 5 spec.
