---
title: "NSS の旧バージョンが原因で一部のセキュアなサイトが動作しません"
date: "2017-01-11T17:12:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["51"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317857"
      title: "Bug 1317857 - There are servers using old and broken versions of NSS"
---
いくつかのセキュアなサーバーが Firefox 51 (および Google Chrome Canary) で動作せず、「[安全な接続ができませんでした](https://support.mozilla.org/ja/kb/secure-connection-failed-error-message)」というエラーページが表示されてしまうことが Mozilla 開発者によって発見されました。[影響を受けるサイト一覧](https://bug1317857.bmoattachments.org/attachment.cgi?id=8811077) はトラッキングバグに添付されていますが、おそらく他にもあるでしょう。

それらのサーバーは [Network Security Services](https://developer.mozilla.org/ja/docs/Mozilla/Projects/NSS) (NSS) ライブラリの旧バージョンを使っているようで、これには `signature_algorithms` の解析処理に [バグがあり](https://bugzilla.mozilla.org/show_bug.cgi?id=1317857#c13)、NSS 3.28 以降を同梱した最新のブラウザ上で `PR_END_OF_FILE_ERROR` を投げるため、より新しいバージョンにアップグレードしなければなりません。
