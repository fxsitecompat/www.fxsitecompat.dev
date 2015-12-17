---
title: "Geolocation API が Firefox 43 以降で動作していません"
date: "2015-12-17T16:05:00-05:00"
categories: ["misc"]
tags: []
versions: ["43", "44", "45", "46"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1232995": "Bug 1232995 - HTML5 Geolocation Not Working After Update to version 43"
---
現在、Mozilla の新しい Google Location Service API キーとその使用回数上限が原因で、Firefox 43 およびそれ以降のバージョンで [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation) が動作していません。Mozilla と Google はともに問題を認識しており、まもなく解決する見込みです。
