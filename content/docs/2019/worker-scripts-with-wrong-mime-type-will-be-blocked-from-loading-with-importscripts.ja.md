---
title: "誤った MIME タイプの Worker スクリプトは `importScripts()` での読み込みがブロックされます"
date: "2019-05-13T04:06:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1514680"
      title: "Bug 1514680 - Consider strictly enforcing MIME checks for `importScripts()`."
aliases:
    - "/ja/docs/2019/worker-script-served-with-wrong-mime-type-will-be-blocked/"
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-importscripts/"
---
Firefox 67 以降、セキュリティ上の理由から、誤った MIME タイプで配信された Worker スクリプトは `importScripts` メソッドで Worker スコープ内に読み込めなくなりました。[Firefox 51](https://www.fxsitecompat.dev/ja/docs/2016/javascript-served-with-wrong-mime-type-will-be-blocked/) で既に同様の変更が通常の JavaScript ファイルを対象に行わています。スクリプトファイルは必ず `text/javascript` もしくは `application/javascript` 配信するよう気を付けてください。

**更新**: [Firefox 70](https://www.fxsitecompat.dev/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/) で同じ変更が `Worker()` や `SharedWorker()` で読み込まれた Worker スクリプトにも適用されました。この記事のタイトルは、Firefox 67 での変更が `importScripts()` にのみ適用されることを明確にするため更新されました。
