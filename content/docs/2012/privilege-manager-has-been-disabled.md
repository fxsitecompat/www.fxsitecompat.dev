---
title: "Privilege Manager has been disabled"
date: "2012-12-03T03:50:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["17"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=757046"
      title: "Bug 757046 – Investigate interim solutions for enablePrivilege"
---
The [Privilege Manager](https://developer.mozilla.org/docs/Bypassing_Security_Restrictions_and_Signing_Code), a JavaScript extension `netscape.security.PrivilegeManager.enablePrivilege` that has been [deprecated since Firefox 12](https://bugzilla.mozilla.org/show_bug.cgi?id=713747), has been disabled. Changing the value of a hidden pref `security.enablePrivilege.enable_for_tests` to `true` can test this feature, but of course it's not recommended. You should find a workaround like an add-on where privileges are actually required.

Since some sites are still using the `netscape.security` object for browser detection, [the object has been temporarily restored](https://bugzilla.mozilla.org/show_bug.cgi?id=791526). From now, use an alternative way to detect browsers.
