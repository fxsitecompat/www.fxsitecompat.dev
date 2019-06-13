---
title: "`window.find()` ダイアログ対応が廃止されました"
date: "2017-04-18T17:18:00-04:00"
categories: ["dom"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672395"
      title: "Bug 672395 - Let's kill window.find()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1348409"
      title: "Bug 1348409 - Assertion failure: XRE_IsParentProcess() with window.find"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gn4364N4TlY/discussion"
      title: "window.find dialog feature broken in Firefox 53 (a.k.a., Late Intent to Unship: window.find's dialog support)"
---
Firefox では、[`window.find`](https://developer.mozilla.org/docs/Web/API/Window/find) メソッドを使って、ユーザーが現在開いているページ上の文字列を見つけられるようにするダイアログを開くことが可能でした。このダイアログは、[`window.showModalDialog`](https://www.fxsitecompat.dev/ja/docs/2016/window-showmodaldialog-has-been-removed/) と同様に、Firefox 48 で e10s と呼ばれているマルチプロセスモードが有効になって以降、機能していないことが判明しました。Firefox 53 以降、ブラウザー内で e10s が無効の場合にもこのダイアログは機能しません。

こうしたページ内検索ダイアログを開くブラウザーは他にないことから、Mozilla 開発者は、機能を復元するよりも `aShowDialog` 引数への対応を明示的に削除することを決定しました。

この非標準メソッドは、完全に削除する計画も以前からあるため、いずれにしても使用は推奨されません。

**更新**: `aShowDialog` 引数対応は Firefox 53.0.2 で削除されました。
