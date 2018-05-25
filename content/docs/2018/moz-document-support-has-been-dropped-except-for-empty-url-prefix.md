---
title: "`@-moz-document` support has been dropped except for empty `url-prefix()`"
date: "2018-03-18T16:09:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1446470"
      title: "Bug 1446470 - Parse @-moz-document url-prefix() on content."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/en-CA/docs/2015/moz-document-support-has-been-dropped/"
    - "/en-CA/docs/2015/moz-document-support-will-be-dropped/"
    - "/en-CA/docs/2018/moz-document-has-been-dropped/"
---
The [`@-moz-document`](https://developer.mozilla.org/docs/Web/CSS/@document) rule is no longer available from Web content since it could be used by attackers for CSS injection to steal private data in the URL of third-party sites. Firefox users are still able to use this rule in the user stylesheet to personalize their browsing experience.

The at-rule support has already been removed from Nightly and early Beta/DevEdition as of Firefox 59, and removed from all the channels with Firefox 61.

An exception is the empty `url-prefix` function that has been used as a [CSS hack targeting Firefox](https://css-tricks.com/snippets/css/css-hacks-targeting-firefox/). It continues to be parsed on the Release channel to avoid breakages but will be removed in the near future once major compatibility issues are solved.
