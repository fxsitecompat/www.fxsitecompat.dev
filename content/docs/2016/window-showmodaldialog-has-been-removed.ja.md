---
title: "`window.showModalDialog()` が削除されました"
date: "2016-06-08T09:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=981796"
      title: "Bug 981796 - Remove window.showModalDialog"
    - url: "https://asadotzler.com/2016/06/06/firefox-48-beta-release-and-e10s/"
      title: "Firefox 48 Beta, Release, and E10S"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/4t5AAxxrCoA/discussion"
      title: "Intent to unship: window.showModalDialog"
aliases:
    - "/ja/docs/2015/window-showmodaldialog-will-be-removed/"
---
[Firefox 28 以降](https://www.fxsitecompat.com/ja/docs/2013/showmodaldialog-has-been-deprecated/) 廃止予定となっており、[Firefox 28 以降](https://www.fxsitecompat.com/ja/docs/2013/showmodaldialog-has-been-deprecated/) ブラウザーが *e10s* と呼ばれるマルチプロセスモードでの実行時には無効化される、レガシーな [`window.showModalDialog`](https://developer.mozilla.org/docs/Web/API/Window/showModalDialog) メソッドが、*e10s* のデフォルト有効化に伴い Firefox 48 以降使用できなくなりました。

Firefox 48 リリースの時点ですべての Firefox ユーザーが *e10s* の恩恵を受けるわけではなく、技術的にはまだ *e10s* が無効の場合にはこのメソッドは存在します。ただ、実質的に廃止されたことを踏まえて、標準の [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) メソッドか独自のページ内モーダル UI を代わりに使ってください。後者の場合、アクセシビリティを確保するため WAI-ARIA の [`dialog` ロール](https://developer.mozilla.org/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_dialog_role) を実装することが推奨されます。残念ながら HTML の [`<dialog>`](https://developer.mozilla.org/docs/Web/HTML/Element/dialog) 要素はまだ Firefox には実装されていません。

**更新**: このメソッドは全ユーザーの Firefox 56 から削除されました。
