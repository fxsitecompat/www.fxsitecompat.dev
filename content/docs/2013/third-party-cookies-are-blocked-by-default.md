---
title: "Third-party cookies are blocked by default"
date: "2013-02-24T03:44:31-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["22"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818340"
      title: "Bug 818340 – Block cookies from sites I haven\'t visited"
---
Starting with Firefox 22, third-party cookies are blocked by default, like Apple Safari, to give users more control over online privacy. For details, see [the post on Mozilla Privacy Blog](https://blog.mozilla.org/privacy/2013/02/25/firefox-getting-smarter-about-third-party-cookies/) and Jonathan Mayer's [FAQ about the new Firefox cookie policy](http://webpolicy.org/2013/02/22/the-new-firefox-cookie-policy/).

<ins>Update: [**This change has been postponed**](https://bugzilla.mozilla.org/show_bug.cgi?id=851606) to collect and analyze data on the effect of blocking some third-party cookies. In the Beta and Release channels, the default preference will be kept to allow third-party cookies. See [Brendan Eich's blog post](https://brendaneich.com/2013/05/c-is-for-cookie/) for details.</ins>

**Update 2**: Starting with [Firefox 65](https://www.fxsitecompat.com/en-CA/docs/2018/third-party-tracking-cookies-are-now-blocked-by-default/), Third-party tracking cookies are blocked by default.
