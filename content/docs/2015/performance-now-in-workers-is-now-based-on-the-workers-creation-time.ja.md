---
title: "ワーカー内の `performance.now` がそのワーカーの作成時刻を基準とするようになりました"
date: "2015-12-17T14:39:00-05:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1169068"
      title: "Bug 1169068 - Update the High Resolution Time API to the latest version of the spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1226147"
      title: "Bug 1226147 - WorkerPrivate->NowBaseTimeStamp() should not return the parent->GetPerformance()->Now() in dedicated Workers."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/PBiil3ItyeY/discussion"
      title: "Intent to implement and ship: Changes to Worker performance.now() zero time"
---
Firefox 45 以降、ワーカー内の [`performance.now`](https://developer.mozilla.org/docs/Web/API/Performance/now) メソッドは、最新の High Resolution Time 仕様に従い、親ウィンドウや親ワーカーから継承された [ナビゲーション開始時刻](https://developer.mozilla.org/docs/Web/API/PerformanceTiming/navigationStart) ではなく、そのワーカーの作成時刻からの [`DOMHighResTimeStamp`](https://developer.mozilla.org/docs/Web/API/DOMHighResTimeStamp) を返します。従来のようにメインウィンドウコンテキストに基づくタイムスタンプを得るには、新しい [`Performance.translateTime`](https://w3c.github.io/hr-time/#dom-performance-translatetime) メソッドを使ってください。

**更新**: 仕様がまだ不安定らしいことから、この変更は Firefox 45 Beta サイクル中に [取り消されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1243881)。
