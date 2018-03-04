---
title: "近いうちに非表示キーが `keypress` イベントを発生させなくなります"
date: "2018-03-03T04:49:00-05:00"
categories: ["dom"]
tags: []
versions: ["60"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1440189"
      title: "Bug 1440189 - Stop dispatching keypress event on web content in Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442528"
      title: "Bug 1442528 - Nightly 2018-03-01 broke keyboard handling in Google Docs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442847"
      title: "Bug 1442847 - No longer possible to navigate through conversations in Gmail using up and down arrow"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wW9el-i5mtA/discussion"
      title: "Intent to stop dispatching \"keypress\" event for non-printable keys and key combinations in Nightly and early Beta"
---
[UI Events 仕様](https://w3c.github.io/uievents/) や他のブラウザーの挙動に合わせるため、Firefox は近い将来、非表示キーや非表示キーの組み合わせに対して `keypress` イベントを発生させないようにします。

[非表示キー](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent/keyCode#Non-printable_keys_(function_keys)) とは、Home、End、Tab、Escape、Backspace、Page Down、矢印といった機能キーのことです。非表示キーの組み合わせには、Ctrl+A、Alt+G、Command+Shift+M といったものが含まれます。ウェブ開発者は代わりに `keydown` イベントを使ってそれらのキーを扱う必要があります。

例外は Enter キーです。修飾キーなしで Enter を押した場合、あるいは Shift+Enter や Ctrl+Enter は、これまで通り `keypress` イベントを発生させます。これは現在の仕様においては正しくありませんが、他のブラウザーと互換性があります。

この変更は Firefox 60 の時点で Nightly と早期 Beta/DevEdition チャンネルに反映されています。主要サイトでの互換性問題が解決し次第、他のチャンネルでもこの標準準拠の挙動が採用されます。今のところ、*Gmail*、*Google Docs* と *Google Sheets* で一部のキーボードショートカットが正常に動作していません。
