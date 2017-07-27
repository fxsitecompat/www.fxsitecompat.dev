---
title: "Intl API がすべてのプラットフォームにおいてブラウザーロケールを既定値として採用するようになりました"
date: "2017-06-20T01:37:00-04:00"
categories: ["javascript"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1346674"
      title: "Bug 1346674 - Migrate all uses of nsILocaleService::GetApplicationLocale to mozILocaleService::GetAppLocale"
---
macOS、Linux および Android 版の Firefox は従来、ECMAScript Internationalization API について、プログラマーによって何もロケールが指定されていない場合、OS のロケール設定を採用していました。Firefox 55 以降では、Windows に限らずすべてのプラットフォームでブラウザーのロケールが既定値として代わりに採用されます。

影響を受けるオブジェクトとメソッドは以下の通りです。

* [`Intl.DateTimeFormat`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/DateTimeFormat)
* [`Date.prototype.toLocaleString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)
* [`Date.prototype.toLocaleDateString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)

これは一部の Firefox ユーザーにとって日付形式の変更につながる可能性があります。例えば、ブラウザーのロケールが `en-US` である一方、プラットフォームでは `en-CA` が使われていた場合、`toLocaleDateString` メソッドの戻り値は `2017-06-20` ではなく `6/20/2017` となるでしょう。

ウェブ開発者は、もし必要ならば、おそらく開かれているページのロケールを使って API のオプション `locales` 引数を指定することで、一貫した結果を得ることができます。
