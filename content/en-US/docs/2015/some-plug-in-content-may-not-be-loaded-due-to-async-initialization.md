---
title: "Some plug-in content may not be loaded due to async initialization"
date: "2015-08-12T22:39:43-04:00"
categories: ["plugins"]
tags: []
versions: ["40"]
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1116806": "Bug 1116806 - Let Asynchronous Plugin Initialization ride the train"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1195607": "Bug 1195607 - Async Plugin Init compatibility issues found on release channel"
---
Firefox 40 has enabled asynchronous plug-in initialization for a better performance, as Aaron Klotz explains in [his blog post](http://dblohm7.ca/blog/2014/06/17/asynchronous-plugin-initialization-an-introduction/). As the side effect, specific plug-in content, such as Flash videos or games including [*FarmVille 2*](https://bugzilla.mozilla.org/show_bug.cgi?id=1194958), may not be loaded properly depending on the code design. If you change the `dom.ipc.plugins.asyncInit` preference value to `false` in `about:config` and your issue can no longer be reproduced, it is caused by the async initialization. Developers are encouraged to [file a bug](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Plug-ins&blocked=1195607) while consulting the corresponding plug-in vendor to work around the issue.

**Update**: Due to considerable breakages, this change was backed out via the [Firefox hotfix add-on](https://bugzilla.mozilla.org/show_bug.cgi?id=1196000) updated on <time datetime="2015-08-19">August 19</time> as well as [Firefox 40.0.3](https://bugzilla.mozilla.org/show_bug.cgi?id=1198590) shipped on <time datetime="2015-08-27">August 27</time>. A [radical solution](https://bugzilla.mozilla.org/show_bug.cgi?id=1194600) to the issue has been created and implemented to Firefox 41.

**Update**: In order to avoid conflict with the hotfix add-on, Firefox 41 has [renamed the preference](https://bugzilla.mozilla.org/show_bug.cgi?id=1200698) to `dom.ipc.plugins.asyncInit.enabled` while the default value (`true`) remains the same.
