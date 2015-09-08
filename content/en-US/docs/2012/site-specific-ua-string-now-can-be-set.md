---
title: "Site-specific UA string now can be set"
date: "2012-12-03T03:50:54-05:00"
categories: ["networking"]
tags: []
versions: "17"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=782453": "Bug 782453 – Add site-specific User Agent infrastructure and use it to fix AOL Mail"
---
[An issue on the AOL's Web mail service](https://bugzilla.mozilla.org/show_bug.cgi?id=778408) was reported that Firefox had been fallbacked to the basic application with limited features if the old build date (`Gecko/20100101`) was not contained in the user agent (UA) string. Mozilla has contacted the webmaster to ask to fix the issue but got no response, so as an immediate workaround, Firefox has implemented a mechanism that can override the UA string for each site and applied that to `aol.com`. Specifically, the value of a hidden preference `general.useragent.override.aol.com` has been set to `Gecko/[^ ]*#Gecko/20100101`.

Starting with [Firefox 4](https://hacks.mozilla.org/2010/09/final-user-agent-string-for-firefox-4/), [the UA string of Firefox](https://developer.mozilla.org/en-US/docs/Gecko_user_agent_string_reference) has sometimes been made minor changes. When you detect browsers, you're recommended to adopt a [feature detection approach](https://developer.mozilla.org/en-US/docs/Browser_Feature_Detection) to see whether specific features (e.g. objects and functions) are implemented, instead of sniffing UA strings that are subject to change.

<ins datetime="2012-10-12">Update on Oct 12: [The hidden pref was removed](https://bugzilla.mozilla.org/show_bug.cgi?id=797363) as AOL has been fixed the issue. The mechanism to override the UA string still remains.</ins>

<ins datetime="2012-11-22">Update on Nov 22: The mechanism has been utilized to workaround site-specific issues on [some online banking sites](https://bugzilla.mozilla.org/show_bug.cgi?id=792054) and [a Web page authoring tool](https://bugzilla.mozilla.org/show_bug.cgi?id=799502).</ins>
