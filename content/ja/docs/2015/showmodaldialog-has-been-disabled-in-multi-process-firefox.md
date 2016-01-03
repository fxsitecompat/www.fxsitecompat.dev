---
title: "`showModalDialog` がマルチプロセス Firefox で無効化されました"
date: "2015-12-29T21:46:00-05:00"
categories: ["dom"]
tags: []
versions: ["46"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1077002": "Bug 1077002 - window.showmodaldialog does not work with e10s"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1234700": "Bug 1234700 - Hide window.showModalDialog, at least when e10s is enabled"
---
[`window.showModalDialog`](https://developer.mozilla.org/ja/docs/Web/API/Window/showModalDialog) メソッドは、Firefox が  [Electrolysis](https://wiki.mozilla.org/Electrolysis) (e10s) というコードネームで呼ばれているマルチプロセスモードで実行中には動作せず、無効化されるようになりました。このメソッドは [Firefox 28 以降廃止予定となっており](https://www.fxsitecompat.com/ja/docs/2013/showmodaldialog-has-been-deprecated/)、現在 Firefox Nightly と [Developer Edition](https://www.fxsitecompat.com/ja/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/) のみで初期設定有効となっている e10s が 2016 年中頃にすべての Firefox チャンネルで有効になると同時に [完全に削除されます](https://www.fxsitecompat.com/ja/docs/2015/window-showmodaldialog-will-be-removed/)。

`showModalDialog` が使えないことで、少なくとも *Office 365* と *Exchange 2016* が正しく動作しないことが判明しています。
