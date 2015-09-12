---
title: "HTTP auth dialog can no longer be triggered by cross-origin resources"
date: "2015-04-27T13:17:23-04:00"
categories: ["privacy-security"]
tags: []
versions: "40"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=647010": "Bug 647010 - Only present HTTP authentication dialogs if it is the top-level document initiating the auth"
---
Firefox, among other browsers, had previously allowed any resources, such as [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe), [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img), [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script), [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) or CSS [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image), to show an HTTP 401 basic authentication dialog. This behavior, however, could be used by attackers to steal the user's credentials if they were able to embed or inject an arbitrary resource to the victimized page. On Firefox 40 and later, the page itself and resources served from the [same origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) can only trigger an authentication dialog, preventing such potential attacks while mitigating site compatibility issues.

If needed, this new behavior can be changed with the hidden `network.auth.allow-subresource-auth` preference taking one of the the following values:

* `0` - Don't allow sub-resources to open HTTP authentication credentials dialogs
* `1` (default) - Allow sub-resources to open HTTP authentication credentials dialogs, but don't allow it for cross-origin sub-resources
* `2` - Allow the cross-origin authentication as well

Source: [modules/libpref/init/all.js](https://dxr.mozilla.org/mozilla-central/source/modules/libpref/init/all.js)

**Update**: In response to the feedback from users, this change was [backed out](https://bugzilla.mozilla.org/show_bug.cgi?id=1197944) from Firefox 41 Beta, 42 Developer Edition and 43 Nightly, so the default value of the `network.auth.allow-subresource-auth` preference has been reverted to `2`. Firefox 40 users should also have received an automatic update to the bundled hotfix add-on, released on <time datetime="2015-09-04">September 4</time>, that [restores the previous behavior](https://bugzilla.mozilla.org/show_bug.cgi?id=1201065).

**Update**: In order to avoid conflict with the hotfix add-on, Firefox 41 has [renamed the preference](https://bugzilla.mozilla.org/show_bug.cgi?id=1202421) to `network.auth.subresource-http-auth-allow` while the possible values and default value (`2`) remain the same.
