---
title: "誤った MIME タイプの Worker スクリプトは `Worker()` や `SharedWorker()` での読み込みがブロックされます"
date: "2020-02-17T15:07:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["75"]
statuses: "postponed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523706"
      title: "Bug 1523706 - Consider strictly enforcing MIME checks for Worker scripts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569122"
      title: "Bug 1569122 - Limit Worker/SharedWorker MIME type blocking to Beta/Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569123"
      title: "Bug 1569123 - Re-enable strict MIME type checking for Worker/SharedWorker"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583657"
      title: "Bug 1583657 - Worker with type \"application/octet-stream\" is blocked on color.adobe.com"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623916"
      title: "Bug 1623916 - Restrict strictly enforcing MIME checks for Worker scripts to early beta or earlier"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EJ9EDv8bqxI/discussion"
      title: "Intent to ship: Blocking Worker/SharedWorker with non-JS MIME type"
aliases:
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-worker-or-sharedworker/"
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/"
    - "/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker-in-nightly-and-early-beta/"
---
Firefox 75 以降、セキュリティ上の理由から、誤った MIME タイプで配信された専用、共有 Worker スクリプトは、それぞれ `Worker()` と `SharedWorker()` による読み込みがブロックされます。この変更は Firefox 70 以降既に Nightly と早期 Beta チャンネルに対して行われていますが、今のところ 1 件しか互換性問題は報告されていません。

[Firefox 67](https://www.fxsitecompat.dev/ja/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-importscripts/) で既に同様の変更が `importScripts()` で読み込まれたスクリプトを対象に行わています。スクリプトファイルは必ず `text/javascript` もしくは `application/javascript` 配信するよう気を付けてください。

**更新**: 新型コロナウイルス (COVID-19) の流行により、人々が自宅でより多くの時間をオンラインで過ごすことを余儀なくされています。こうした不安定な時期に Firefox 75 で変更を行うことに関して懸念の声が上がったため、今後のバージョンに延期されました。早期ベータ版と Nightly チャンネルでは引き続きブロックの強制は有効となります。状況が変わり次第このドキュメントを更新します。
