---
title: "Multi-process is enabled by default on the Developer Edition"
date: "2015-08-05T00:48:18-04:00"
categories: ["misc"]
tags: []
versions: ["43"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1188605"
      title: "Bug 1188605 - Turn e10s on by default for 42/aurora"
---
Starting with Firefox 42, the new multi-process mode called [Electrolysis](https://wiki.mozilla.org/Electrolysis) (e10s) is enabled by default on the [Firefox Developer Edition](https://developer.mozilla.org/Firefox/Developer_Edition) (Aurora) in addition to Firefox Nightly. Since e10s involves numerous drastic changes to the Firefox core, many Web features are still not working properly. See the [dependency tree of Bug 516752](https://bugzilla.mozilla.org/showdependencytree.cgi?id=516752&maxdepth=1&hide_resolved=1) for the open issues, and please file a bug if you have encountered any other problem. Note that some issues may occur when e10s is *disabled*, like [Bug 1188818](https://bugzilla.mozilla.org/show_bug.cgi?id=1188818).

**Update**: This change has been [postponed to Firefox 43](https://bugzilla.mozilla.org/show_bug.cgi?id=1203184) due to the "less coverage of non-e10s testing".
