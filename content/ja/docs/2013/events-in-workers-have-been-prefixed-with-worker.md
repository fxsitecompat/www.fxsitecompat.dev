---
title: "ワーカー内のイベントに `Worker` 接頭辞が付きました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887236"
      title: "Bug 887236 – prefix the current events in workers with \"Worker\""
---
[通常の DOM イベント](https://developer.mozilla.org/ja/docs/Web/Reference/Events) を [Web ワーカー](https://developer.mozilla.org/ja/docs/Web/Guide/Performance/Using_web_workers) 内で使えるようにするため、ワーカー内の既存イベントである [`Event`](https://developer.mozilla.org/ja/docs/Web/API/Event)、[`MessageEvent`](https://developer.mozilla.org/ja/docs/Web/API/MessageEvent)、[`ErrorEvent`](https://developer.mozilla.org/ja/docs/Web/API/ErrorEvent)、[`ProgressEvent`](https://developer.mozilla.org/ja/docs/Web/API/ProgressEvent) が、`WorkerEvent`、`WorkerMessageEvent`、`WorkerErrorEvent`、`WorkerProgressEvent` に改名されました。この変更は**一時的なもの**です。Firefox のバックエンド実装が修正され次第、これらのイベントは再度接頭辞が外れます。
