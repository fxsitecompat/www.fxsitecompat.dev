---
title: "`@-moz-document` support has been dropped"
date: "2018-03-18T16:09:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["61"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1426068"
      title: "Bug 1426068 - Disabling @-moz-document results in users being unable to enter line-breaks into YouTube comments"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/en-CA/docs/2015/moz-document-support-has-been-dropped/"
    - "/en-CA/docs/2015/moz-document-support-will-be-dropped/"
---
The [`@-moz-document`](https://developer.mozilla.org/en-US/docs/Web/CSS/@document) rule is no longer available from Web content since it could be used by attackers for CSS injection to steal private data in the URL of third-party sites. Firefox users are still able to use this rule in their user stylesheet to personalize the browsing experience.

The at-rule support has already been removed from Nightly and early Beta/DevEdition as of Firefox 59, and completely removed from all the channels with Firefox 61.

*YouTube* comments were known to be broken due to this change, but Google has fixed the compatibility issue. Glitches on the *Air Canada* and *Telegram* websites have been solved in Firefox side. Given the situation, there are still chances of other sites being affected.
