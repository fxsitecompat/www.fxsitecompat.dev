---
title: "クロスサイト `XMLHttpRequest` が `Origin` ヘッダの欠如によりブロックされてしまいます"
date: "2016-02-07T22:27:00-05:00"
categories: ["networking"]
tags: []
versions: ["43", "44"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1243453": "Bug 1243453 - Missing Origin header in Cross Origin Request resulting in Cross-Origin Request Blocked"
---
Firefox 43 で、[クロスサイト `XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) に関するリグレッションが発生しました。`GET` リクエストに `Origin` ヘッダが欠落しており、結果として不要なプレフライト `OPTIONS` リクエストが行われ、それに失敗した `GET` リクエストが続いていました。このバグは Firefox 45 で修正されました。
