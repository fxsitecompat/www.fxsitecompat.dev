---
title: "XHR `responseURL` にフラグメントが含まれなくなりました"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1073882"
      title: "Bug 1073882 – XMLHttpRequest.prototype.responseURL should not have fragment per latest spec"
---
[`XMLHttpRequest.responseURL`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest.responseURL) プロパティによって返される レスポンス URL が、最新の [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) 仕様に従い、ハッシュ (`#`) で始まるフラグメントを含まない形式となりました。
