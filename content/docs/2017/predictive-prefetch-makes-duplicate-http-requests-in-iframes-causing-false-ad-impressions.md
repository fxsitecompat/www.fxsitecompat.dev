---
title: "Predictive prefetch makes duplicate HTTP requests in iframes, causing false ad impressions"
date: "2017-03-30T11:38:00-04:00"
categories: ["networking"]
tags: []
versions: ["52", "52-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349921"
      title: "Bug 1349921 - Cached iframe executes previously loaded and dynamically inserted scripts, makes network calls before \"onload\" event."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1350032"
      title: "Bug 1350032 - Google seeing duplicate requests to custom URIs that should only be requested once"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1351082"
      title: "Bug 1351082 - System addon to disable predictive prefetch"
    - url: "https://mail.mozilla.org/pipermail/gofaster/2017-March/000655.html"
      title: "Intent to implement & ship: disable network predictor prefetch"
---
Online advertising network companies have reported to Mozilla that they are observing a lot of duplicate impressions coming from Firefox 52 users. This issue has turned out to be a bug in the newly enabled network predictor prefetch service, making repeated GET requests even to the URL of scripts or images dynamically inserted inside inline frames.

The predictive prefetch feature will be disabled in Firefox 52 soon remotely, and re-enabled in Firefox 55 once the issue is examined and solved.
