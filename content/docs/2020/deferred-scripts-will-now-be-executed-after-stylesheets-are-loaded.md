---
title: "Deferred scripts will now be executed after stylesheets are loaded"
date: "2020-04-06T23:15:00-04:00"
categories: ["css", "html", "javascript"]
tags: []
versions: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1622235"
      title: "Bug 1622235 - <script defer> should wait for stylesheet loads."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/VXlDBa3SvWA/discussion"
      title: "Intent to prototype and ship: Make <script defer> wait for stylesheet loads."
---
The WHATWG community has [discussed](https://github.com/whatwg/html/issues/3890) the inconsistent behaviour of `<script defer>`, that should wait for stylesheets being loaded as per the spec but no browsers other than the legacy version of Microsoft Edge had done it. This problem was causing a [flash of unstyled content](https://en.wikipedia.org/wiki/Flash_of_unstyled_content) (FOUC) on various websites particularly in Firefox.

Firefox 76 has solved the issue, and deferred scripts, including modules deferred by default, will be executed after all stylesheets are loaded. Web developers need to expect inconsistent rendering behaviour until the change is implemented by other modern browsers.
