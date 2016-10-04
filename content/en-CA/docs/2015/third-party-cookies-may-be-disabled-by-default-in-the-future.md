---
title: "Third-party cookies may be disabled by default in the future"
date: "2015-10-27T14:54:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818340"
      title: "Bug 818340 - Block cookies from sites I haven't visited"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=851606"
      title: "Bug 851606 - Disable bug 818340 for Beta until we're ready"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=999170"
      title: "Bug 999170 - Back out bug 851606 to enable bug 818340 on the default 3rd-party cookie policy for releases"
---
There is a lengthy discussion about [third-party cookies](https://support.mozilla.org/en-US/kb/disable-third-party-cookies) and privacy. This change was [originally planned for Firefox 22](https://www.fxsitecompat.com/en-CA/docs/2013/third-party-cookies-are-blocked-by-default/) but reverted on the Beta and Release channels due to obvious compatibility issues. Third-party cookies have been disabled by default on the [Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) and Nightly channels, the relevant bug is still open, and now [Firefox 42 features Private Browsing with Tracking Protection](https://www.fxsitecompat.com/en-CA/docs/2015/private-browsing-now-comes-with-tracking-protection/). Though there is not clear timeline yet, this topic is worth your attention.
