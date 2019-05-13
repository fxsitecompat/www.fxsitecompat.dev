---
title: "誤った MIME タイプで配信されたワーカースクリプトはブロックされます"
date: "2019-05-13T04:06:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1514680"
      title: "Bug 1514680 - Consider strictly enforcing MIME checks for `importScripts()`."
---
Firefox 67 以降、セキュリティ上の理由から、誤った MIME タイプで配信されたワーカースクリプトは `importScripts` メソッドでワーカースコープ内に読み込めなくなりました。[Firefox 51](https://www.fxsitecompat.com/ja/docs/2016/javascript-served-with-wrong-mime-type-will-be-blocked/) で既に同様の変更が通常の JavaScript ファイルを対象に行わています。スクリプトファイルは必ず `text/javascript` もしくは `application/javascript` 配信するよう気を付けてください。
