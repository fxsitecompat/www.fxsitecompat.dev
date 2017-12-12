---
title: "`@-moz-document` support will be dropped"
date: "2015-10-13T13:17:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423331"
      title: "Bug 1423331 - telegram text box cursor is confused when focusing both window and textbox in 59.0a1 (2017-12-05) (64-bit)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1424633"
      title: "Bug 1424633 - Can't check in to flight on aircanada.ca"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/en-CA/docs/2015/moz-document-support-has-been-dropped/"
---
The [`@-moz-document`](https://developer.mozilla.org/en-US/docs/Web/CSS/@document) rule will no longer be available from Web content since it could be used by attackers for CSS injection to steal private data in the URL of third-party sites. Firefox users are still able to use this rule in their user stylesheet to personalize the browsing experience.

**Update**: An earlier draft of this document said the change was made with Firefox 44, but the patch was not merged to that version due to a [layout compatibility issue](https://bugzilla.mozilla.org/show_bug.cgi?id=504622) on the `<fieldset>` element. The bug is expected to be solved soon.

**Update 2**: The at-rule support has been removed again from Nightly and early Beta as of Firefox 59. It will soon be completely dropped.

**Update 3**: The websites of *Air Canada* and *Telegram* are known to be broken due to this change.
