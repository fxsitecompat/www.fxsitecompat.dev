---
title: "非 HTTP XHR がステータスコード `200` を返すようになりました"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=716491"
      title: "Bug 716491 – Investigate the status code for non-HTTP XHR."
---
成功した非 HTTP [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) レスポンスのステータスコードが、仕様に従って `0` から `200` へ変更されました。
