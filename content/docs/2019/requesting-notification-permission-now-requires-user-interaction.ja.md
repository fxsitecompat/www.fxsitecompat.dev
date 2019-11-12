---
title: "通知許可リクエストがユーザーインタラクションを必要とするようになりました"
date: "2019-11-11T20:16:00-05:00"
categories: ["dom"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592959"
      title: "Bug 1592959 - Warn about non-user interaction Notification requests"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1593644"
      title: "Bug 1593644 - Enable dom.webnotifications.requireuserinteraction on Release"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Mezd5pLjnJU/discussion"
      title: "Intent to Ship: Require user interaction for notification permission prompts"
    - url: "https://blog.mozilla.org/futurereleases/2019/11/04/restricting-notification-permission-prompts-in-firefox/"
      title: "Restricting Notification Permission Prompts in Firefox - Future Releases"
aliases:
    - "/ja/docs/2019/requesting-notification-permission-will-soon-require-user-interaction/"
---
Firefox では従来ブラウザー内でのユーザーインタラクションなしにプッシュ通知の許可を求めることが可能でしたが、プロンプトスパムを防ぐ取り組みの一環として、そうした手法は Firefox 72 で機能しなくなりました。Nightly と早期 Beta/DevEdition チャンネルでは Firefox 68 以降既にユーザーインタラクションが必要とされており、Firefox 71 ではそのような事例に対してウェブコンソールに廃止予定の警告が表示されます。

[`Notification.requestPermission`](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)、[`PushManager.subscribe`](https://developer.mozilla.org/docs/Web/API/PushManager/subscribe) 両メソッドは常に `click` や `keydown` といった短時間で実行されるユーザー生成イベントハンドラーの内部から呼び出さなければなりません。
