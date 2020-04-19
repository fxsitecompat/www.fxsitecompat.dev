---
title: "`feed` and `pcast` protocols are no longer supported"
date: "2017-12-26T10:36:00-05:00"
categories: ["misc"]
tags: []
releases: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1420622"
      title: "Bug 1420622 - Remove Feed and Pcast related protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/abHJ-jaQ5YY/discussion"
      title: "Intent to remove pcast and feed protocols"
---
Firefox 59 has removed the support for the `feed` and `pcast` protocols for web feed handling, which were never standardized or implemented in other browsers. The built-in feed preview functionality will continue working with `https` or `http` feed URLs without one of these protocols, so there should be no risk of the removal.
