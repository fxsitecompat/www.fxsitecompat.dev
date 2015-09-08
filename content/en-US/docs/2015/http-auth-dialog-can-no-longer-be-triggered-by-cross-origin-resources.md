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
Firefox, among other browsers, had previously allowed any resources, such as [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe), [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img), [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script), [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) or CSS [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image), to show an HTTP 401 basic authentication dialog. This behavior, however, could be used by attackers to steal the user's credentials if they were able to embed or inject an arbitrary resource to the victimized page. On Firefox 40 and later, the page itself and resources served from the [same origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) can only trigger an authentication dialog, preventing such potential attacks while mitigating site compatibility issues. This new behavior can be changed with the hidden `network.auth.allow-subresource-auth` preference if needed; see [`all.js`](https://mxr.mozilla.org/mozilla-central/source/modules/libpref/init/all.js#1779) for the possible values.

**Update**: In response to feedback from users, this change was [backed out](https://bugzilla.mozilla.org/show_bug.cgi?id=1197944) from Firefox 41 Beta, 42 Developer Edition and 43 Nightly. Firefox 40 users should have received an automatic update to the [bundled hotfix add-on](https://bugzilla.mozilla.org/show_bug.cgi?id=1201065), released on <time datetime="2015-09-04">September 4</time>, that restores the previous behavior.
