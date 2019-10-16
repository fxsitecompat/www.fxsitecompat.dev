---
title: "Nightly と早期ベータ版で誤った MIME タイプの Worker スクリプトは `Worker()` や `SharedWorker()` での読み込みがブロックされます"
date: "2019-07-24T07:00:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523706"
      title: "Bug 1523706 - Consider strictly enforcing MIME checks for Worker scripts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569122"
      title: "Bug 1569122 - Limit Worker/SharedWorker MIME type blocking to Beta/Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569123"
      title: "Bug 1569123 - Re-enable strict MIME type checking for Worker/SharedWorker"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583657"
      title: "Bug 1583657 - Worker with type \"application/octet-stream\" is blocked on color.adobe.com"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EJ9EDv8bqxI/discussion"
      title: "Intent to ship: Blocking Worker/SharedWorker with non-JS MIME type"
aliases:
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-worker-or-sharedworker/"
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/"
---
Firefox 70 以降、セキュリティ上の理由から、誤った MIME タイプで配信された専用、共有 Worker スクリプトは、それぞれ `Worker()` と `SharedWorker()` による読み込みがブロックされます。この変更は Nightly と早期 Beta チャンネルに対して行われ、開発者が互換性を評価しています。

[Firefox 67](https://www.fxsitecompat.dev/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-importscripts/) で既に同様の変更が `importScripts()` で読み込まれたスクリプトを対象に行わています。スクリプトファイルは必ず `text/javascript` もしくは `application/javascript` 配信するよう気を付けてください。

**更新**: この変更は今のところ非 Release チャンネルでしか行われていないため、タイトルと内容を更新しました。

**更新 2**: *Adobe Color* がこの変更により正常に動作していないことが判明しています。
