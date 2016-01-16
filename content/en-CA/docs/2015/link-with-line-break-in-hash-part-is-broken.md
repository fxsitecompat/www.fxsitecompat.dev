---
title: "Link with line break in hash part is broken"
date: "2015-10-20T21:43:00-07:00"
categories: ["networking"]
tags: [""]
versions: ["38", "39", "40", "41"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1189852": "Bug 1189852 - link broken which a line break on hash part after Bug 1144398"
---
On Firefox 38 and later, HTML links containing a newline character in the fragment followed by `#` are broken because it's not allowed by the URL spec and the browser now enforces the constraint. In order to avoid site compatibility issues, this behaviour has been modified with Firefox 42 so the browser will just strip `\r` (CR), `\n` (LF) and `\t` (tab) characters in the hash part. Links containing `\0` (null) are still rejected.
