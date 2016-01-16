---
title: "Non-SSL active content on SSL pages is blocked by default"
date: "2013-04-06T04:52:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["23"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=834836": "Bug 834836 – Turn on pref to block mixed active content"
---
[Firefox 18](https://www.fxsitecompat.com/en-CA/docs/2012/fyi-preferences-to-prevent-non-ssl-contents-on-ssl-pages-from-loading-have-been-added/) introduced preferences to block loading content from non-SSL (`http`) sites on SSL (`https`) pages. One of those preferences, `security.mixed_content.block_active_content` is now enabled by default in order to enhance user security. That means insecure scripts, stylesheets, plug-in contents, [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe), [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest), Web fonts ([`@font-face`](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face)) and [WebSockets](https://developer.mozilla.org/en-US/docs/WebSockets) are blocked on secure pages, and a notification is displayed instead. It will **not** block "display content" like images, videos or audio. See [Tanvi Vyas' blog post](https://blog.mozilla.org/tanvi/2013/04/10/mixed-content-blocking-enabled-in-firefox-23/) for details.

Mozilla is tracking mixed content issues found on [major sites](https://bugzilla.mozilla.org/showdependencytree.cgi?id=844556) as well as [its own properties](https://bugzilla.mozilla.org/showdependencytree.cgi?id=843977).
