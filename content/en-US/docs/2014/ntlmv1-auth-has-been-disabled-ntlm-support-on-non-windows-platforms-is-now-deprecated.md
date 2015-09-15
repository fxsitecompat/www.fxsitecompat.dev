---
title: "NTLMv1 auth has been disabled, NTLM support on non-Windows platforms is now deprecated"
date: "2014-03-21T04:50:04-04:00"
categories: ["privacy-security"]
tags: []
versions: "30"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=828183": "Bug 828183 – Firefox enables insecure NTLM (pre-NTLMv2) authentication"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999306": "Bug 999306 – Allow generic NTLM v1 if pref set"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1023748": "Bug 1023748 – Allow NTLMv1 over SSL/TLS, or intranet access is broken on Firefox 30 for non-Windows platforms"
---
The support for the NT LAN Manager version 1 (NTLMv1) network authentication has been disabled because it's known as insecure. Companies and organizations still deploying the older protocol should upgrade to NTLMv2. See [Honza Bambas' blog post](http://www.janbambas.cz/ntlm-v1-and-firefox/) and [Jason Duell's post to the dev-planning list](https://groups.google.com/d/topic/mozilla.dev.planning/JbrpDmqDLXI) for details.

This is affecting *SharePoint*-based or *IIS*-backed intranet applications. If you encounter any problems on Firefox 30 or later, you can manually enable NTLMv1 using a preference. Note that NTLMv2 is not supported on non-Windows platforms, so OS X and Linux users have to toggle the preference to continue using NTLMv1 as below, though the NTLM auth support on non-Windows platforms is considered deprecated.

How to enable NTLMv1: type `about:config` in the location bar, click the "I'll be careful" button, find `network.negotiate-auth.allow-insecure-ntlm-v1`, double-click on it to change the value to `true`.

Another workaroud here is using [Firefox 24 <abbr title="Extended Support Release">ESR</abbr>](https://www.mozilla.org/en-US/firefox/organizations/) that still enables the NTLMv1 auth.
