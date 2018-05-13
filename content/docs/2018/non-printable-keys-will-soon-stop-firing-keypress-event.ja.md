---
title: "近いうちに非表示キーが `keypress` イベントを発生させなくなります"
date: "2018-03-03T04:49:00-05:00"
categories: ["dom"]
tags: []
versions: ["61"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1440189"
      title: "Bug 1440189 - Stop dispatching keypress event on web content in Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442528"
      title: "Bug 1442528 - Keyboard handling in Google Docs is broken if \"dom.keyboardevent.keypress.dispatch_non_printable_keys_only_system_group_in_content\" is true"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454833"
      title: "Bug 1454833 - Keyboard shortcuts do not work on hangouts.google.com in strict keypress event dipatching mode"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455059"
      title: "Bug 1455059 - Tab no longer works in Etherpad"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455229"
      title: "Bug 1455229 - Add Google Keep into the blacklist to use legacy keypress event behavior"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1456038"
      title: "Bug 1456038 - Google Inbox Keyboard Shortcuts Broken"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457247"
      title: "Bug 1457247 - Add www.rememberthemilk.com into \"dom.keyboardevent.keypress.hack.dispatch_non_printable_keys\""
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1459800"
      title: "Bug 1459800 - Add \"papaer.dropbox.com/doc\" into the blacklist to allow to dispatch keypress events even for non-printable keys"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wW9el-i5mtA/discussion"
      title: "Intent to stop dispatching \"keypress\" event for non-printable keys and key combinations in Nightly and early Beta"
---
[UI Events 仕様](https://w3c.github.io/uievents/) や他のブラウザーの挙動に合わせるため、Firefox は近い将来、非表示キーや非表示キーの組み合わせに対して `keypress` イベントを発生させないようにします。

[非表示キー](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/keyCode#Non-printable_keys_(function_keys)) とは、Home、End、Tab、Escape、Backspace、Page Down、矢印といった機能キーのことです。非表示キーの組み合わせには、Ctrl+A、Alt+G、Command+Shift+M といったものが含まれます。ウェブ開発者は代わりに `keydown` イベントを使ってそれらのキーを扱う必要があります。

例外は Enter キーです。修飾キーなしで Enter を押した場合、あるいは Shift+Enter や Ctrl+Enter は、これまで通り `keypress` イベントを発生させます。これは現在の仕様においては正しくありませんが、他のブラウザーと互換性があります。

この変更は Firefox 60 の時点で Nightly と早期 Beta/DevEdition チャンネルに反映されています。主要サイトでの互換性問題が解決し次第、他のチャンネルでもこの標準準拠の挙動が採用されます。今のところ、*Gmail*、*Google Docs* と *Google Sheets* で一部のキーボードショートカットが正常に動作していません。

**更新**: この更新は、元々 Google から要求されたものですが、Google のエンジニアに自社アプリの問題を修正する時間を与えるため、一時的に [バックアウトされました](https://bugzilla.mozilla.org/show_bug.cgi?id=1443117)。

**更新 2**: この変更は Firefox 61 Nightly で再度投入されましたが、今のところ *Gmail*、*Google Docs*、*Google Sheets*、*Google Slides* 上では不具合を避けるため無効化されています。

**更新 3**: *Dropbox Paper*、*Google Hangouts*、*Google Inbox*、*Google Keep*、*Remember The Milk*、さらに主要な公開 *Etherpad* インスタンスも、それらの開発者が問題を修正する時間を持てるよう、ブラックリストへ追加されました。

もしあなたがこれらのアプリのいずれかの開発者で、新たな挙動をテストしたい場合は、次のようにしてブラウザーの設定エディターを使い、ブラックリストを上書きする必要があります。Firefox で [`about:config`](https://support.mozilla.org/kb/about-config-editor-firefox) を開き、`dom.keyboardevent.keypress.hack.dispatch_non_printable_keys` を検索し、その上でクリック、値を空にして、最後に OK をクリックします。
