---
title: "ParallelJS has been removed (Nightly only)"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
releases: ["37", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1117724"
      title: "Bug 1117724 – [meta] Remove PJS"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1118084"
      title: "Bug 1118084 – Remove self-hosted and user-exposed methods from PJS"
---
The development of [ParallelJS (PJS)](http://wiki.ecmascript.org/doku.php?id=strawman:data_parallelism) has been discontinued due to the limited future prospects, little attention and code complexity. The experimental implementation that had been enabled only on the Nightly channel, including the `Array.prototype.mapPar`, `filterPar` and `reducePar` methods, has been completely removed.
