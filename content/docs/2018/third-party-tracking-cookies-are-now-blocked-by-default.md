---
title: "Third-party tracking cookies are now blocked by default"
date: "2018-11-22T01:28:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["65"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492549"
      title: "Bug 1492549 - Enable blocking access to storage from tracking resources by default on all desktop platforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492563"
      title: "Bug 1492563 - Enable blocking access to storage from tracking resources by default on all desktop platforms on Nightly"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oFZivEmLC40/discussion"
      title: "Intent to implement and ship: New cookie jar policy to block storage access from tracking resources"
aliases:
    - "/en-CA/docs/2015/third-party-cookies-may-be-disabled-by-default-in-the-future/"
---
Firefox 65 has enabled [Content Blocking](https://support.mozilla.org/kb/content-blocking) by default on all desktop platforms, which means storage access by tracking resources, including third-party tracking cookies, will be blocked on the browser from now on.

Blocking of third-party cookies was originally planned for [Firefox 22](https://www.fxsitecompat.com/en-CA/docs/2013/third-party-cookies-are-blocked-by-default/) but the change wasn't shipped due to obvious compatibility issues. Later in 2015, [Firefox 42](https://fxsitecompat.com/en-CA/docs/2015/private-browsing-now-comes-with-tracking-protection/) introduced Tracking Protection in the Private Browsing mode, then [Firefox Focus](https://blog.mozilla.org/blog/2015/12/07/focus-by-firefox-content-blocking-for-the-open-web/) was also released. Both products rely on [Disconnect's public blacklist](https://github.com/disconnectme/disconnect-tracking-protection) to identify tracking resources including advertising trackers, analytics code and social share buttons.

While Apple adds [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/) to Safari, Mozilla has [shifted its position](https://blog.mozilla.org/futurereleases/2018/08/30/changing-our-approach-to-anti-tracking/) to enable Tracking Protection by default, starting with [Firefox for iOS](https://blog.mozilla.org/blog/2018/04/12/latest-firefox-for-ios-now-available-with-tracking-protection-by-default/). This functionality, now called Content Blocking, has been experimented on the Beta channel since Firefox 63 and enabled by default on the Nightly channel since Firefox 64.

Web developers and site owners: please make sure that all the site features work properly with Content Blocking enabled. Read the [storage access policy document](https://developer.mozilla.org/docs/Mozilla/Firefox/Privacy/Storage_access_policy) written by Mozilla's privacy engineer to get started. Mozilla also tracks embedded [video](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1400025), [images](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1470301), [comments](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1486425) and [login](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1470298) issues, which might be helpful to grasp common mistakes.

**Update**: This change has been [reverted in Firefox 65](https://bugzilla.mozilla.org/show_bug.cgi?id=1514853), and [another attempt for Firefox 66](https://bugzilla.mozilla.org/show_bug.cgi?id=1525727) has also been backed out. We'll continue monitoring future changes.
