---
title: "通知許可リクエストが近々ユーザーインタラクションを必要とするようになります"
date: "2019-11-01T23:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592959"
      title: "Bug 1592959 - Warn about non-user interaction Notification requests"
    - url: "https://blog.nightly.mozilla.org/2019/04/01/reducing-notification-permission-prompt-spam-in-firefox/"
      title: "Reducing Notification Permission Prompt Spam in Firefox – Firefox Nightly News"
---
Firefox では今のところブラウザー内でのユーザーインタラクションなしにプッシュ通知の許可を求めることが可能ですが、プロンプトスパムを防ぐ取り組みの一環として、そうした手法は近い将来機能しなくなります。Nightly と早期 Beta/DevEdition チャンネルでは Firefox 68 以降既にユーザーインタラクションが必要とされています。Firefox 72 以降、そのような事例に対して、ウェブコンソールに廃止予定の警告が表示されます。[`Notification.requestPermission`](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) メソッドは常に `click` や `keydown` といった短時間で実行されるユーザー生成イベントハンドラーの内部から呼び出さなければなりません。
