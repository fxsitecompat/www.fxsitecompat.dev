---
title: "誤った MIME タイプで配信された JavaScript はブロックされます"
date: "2016-09-07T01:38:00-04:00"
categories: ["javascript", "privacy-security"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1288361"
      title: "Bug 1288361 - Return a network error for requests whose type is \"script\" and response has a MIME type that starts with image/"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299267"
      title: "Bug 1299267 - Return a network error for requests whose type is \"script\" with additional bad MIME types"
---
Firefox 51 以降、`image/*`、`audio/*`、`video/*` あるいは `text/csv` といった誤った MIME タイプで配信された JavaScript ファイルはセキュリティ上の理由から読み込まれず、`NetworkError` が投げられます。HTML `<script>` 要素、`new Worker()`、`new SharedWorker()`、[`importScripts`](https://developer.mozilla.org/docs/Web/API/WorkerGlobalScope/importScripts) メソッドがすべて影響を受けます。あなたのスクリプトが `text/javascript` や `application/javascript` といった適切なタイプで配信されていることを確認してください。
