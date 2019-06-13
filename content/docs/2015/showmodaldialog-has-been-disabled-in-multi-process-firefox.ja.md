---
title: "`showModalDialog()` がマルチプロセス Firefox で無効化されました"
date: "2015-12-29T21:46:00-05:00"
categories: ["dom"]
tags: []
versions: ["46"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1077002"
      title: "Bug 1077002 - window.showmodaldialog does not work with e10s"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1234700"
      title: "Bug 1234700 - Hide window.showModalDialog, at least when e10s is enabled"
---
[`window.showModalDialog`](https://developer.mozilla.org/docs/Web/API/Window/showModalDialog) メソッドは、Firefox が [Electrolysis](https://wiki.mozilla.org/Electrolysis) (*e10s*) というコードネームで呼ばれているマルチプロセスモードで実行中には使用不可能となっています。Firefox が投げていた例外により、少なくとも *Office 365* と *Exchange 2016* が正しく動作しないことが判明していました。

*e10s* 上でこの機能に対応することは技術的に難しいことと、このメソッドは既に [Firefox 28 以降廃止予定](https://www.fxsitecompat.dev/ja/docs/2013/showmodaldialog-has-been-deprecated/) となっていることから、エラーを修正する代わりに `window` から `showModalDialog` を隠す措置が Firefox 46 で講じられました。*Office 365* と *Exchange 2016* はそれぞれの機能判別のおかげで再び動作するようになりました。

今のところ、*e10s* は Firefox Nightly と [Developer Edition](https://www.fxsitecompat.dev/ja/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/) のみで初期設定有効となっています。2016 年中頃にすべての Firefox チャンネルで *e10s* が有効になると同時に、このメソッドは Firefox では [一切使用できなくなります](https://www.fxsitecompat.dev/ja/docs/2015/window-showmodaldialog-will-be-removed/)。

**更新**: *e10s* が初期設定で有効化されたことに伴い、このメソッドは [Firefox 48](https://www.fxsitecompat.dev/ja/docs/2016/window-showmodaldialog-has-been-removed/) 以降では使用できなくなりました。
