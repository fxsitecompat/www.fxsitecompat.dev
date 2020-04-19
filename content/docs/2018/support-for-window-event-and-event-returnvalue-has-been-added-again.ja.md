---
title: "`window.event` と `Event.returnValue` への対応が再度追加されました"
date: "2018-12-24T19:40:00-05:00"
categories: ["dom"]
tags: []
releases: ["66", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=218415"
      title: "Bug 218415 - Request for window.event object added to DOM to ease cross browser scripting"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1452569"
      title: "Bug 1452569 - Implement Event's returnValue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1479964"
      title: "Bug 1479964 - Tracking event.keyCode issue due to the implementation of window.event"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496288"
      title: "Bug 1496288 - Ship Window.event, keyCode change, and keypress event handling changes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/riVG9FqN9iM/discussion"
      title: "Intent to ship: window.event"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/IWLLJmoGroA/discussion"
      title: "Intent to ship: set keyCode or charCode of \"keypress\" event to the other's non-zero value"
---
Firefox 65 で、Internet Explorer 由来の [`window.event`](https://developer.mozilla.org/docs/Web/API/Window/event)、[`Event.prototype.returnValue`](https://developer.mozilla.org/docs/Web/API/Event/returnValue) 両プロパティへの対応が再度追加されました。これは一度 [Firefox 63](https://www.fxsitecompat.dev/en-CA/docs/2018/support-for-event-returnvalue-has-been-added/) で投入されたものの、いくつかのサイト互換性問題から Nightly 以外のチャンネルではすぐに無効化されていました。

Firefox 65 以降、`keypress` イベントの `keyCode` プロパティが `0` の場合、その値は `charCode` と同じになります。逆に、`charCode` が `0` の場合、その値は `keyCode` と同じになります。このミラーリング挙動は他のブラウザーと一致し、互換性問題の大半を解決するものと期待されていますが、既に [Google によって解決されている](https://github.com/google/closure-library/issues/932) *Closure Library* のように、ユーザーエージェント判別が別の問題を引き起こす可能性があります。

ウェブ開発者はまた、これらの旧非標準プロパティをブラウザー判別に使うのを避けるべきです。

**更新**: この変更は *Confluence* のコメントエディターにおける [入力問題](https://bugzilla.mozilla.org/show_bug.cgi?id=1514940) に対処するため [Firefox 66 へ延期されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1520756)。
