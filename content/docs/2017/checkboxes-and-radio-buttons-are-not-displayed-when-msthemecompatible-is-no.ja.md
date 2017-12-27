---
title: "`MSThemeCompatible` が `no` の場合にチェックボックスやラジオボタンが表示されません"
date: "2017-06-17T01:45:00-04:00"
categories: ["html"]
tags: []
versions: ["54"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=169373"
      title: "Bug 169373 - Use nsITheme with HTML form controls"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=605985"
      title: "Bug 605985 - -moz-appearance:none should make checkboxes and radios be non-replaced elements (except on Android)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=966240"
      title: "Bug 966240 - Drop support for MSThemeCompatible"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1373417"
      title: "Bug 1373417 - Checkboxes and radio buttons are not displayed on Firefox 54+ when <meta http-equiv=\"MSTHEMECOMPATIBLE\" content=\"no\"> is specified"
aliases:
    - "/ja/docs/2017/checkboxes-and-radio-buttons-are-not-displayed-when-msthemecompatible-is-disabled/"
---
Firefox 54 で HTML チェックボックスやラジオボタンの描画方法が変更され、`-moz-appearance:none` によるスタイル指定が `<input type="radio">` や `<input type="checkbox">` に対して行われた場合に [置換要素](https://developer.mozilla.org/ja/docs/Web/CSS/Replaced_element) となってしまう問題が解消されました。これにより、ウェブ開発者はより柔軟にフォームコントロールをデザインできるようになります。

しかしながら、ドキュメントの `<head>` 内に `<meta http-equiv="MSThemeCompatible" content="no">` が存在するとそれらの要素が見えなくなってしまうという、思わぬ副作用がこの変更によってもたらされました。

[MSDN の記事](https://msdn.microsoft.com/en-us/library/ms533876(v=vs.85).aspx) によれば、当該の `<meta>` タグは Windows XP 向け Internet Explorer 上で「ドキュメントのテーマ対応を無効化する」もので、Firefox も長いこと部分的な互換性を保ってきました。一方、Google Chrome や Microsoft Edge など他のどのブラウザーもこの非標準の無名機能に対応していません。

問題となった描画リグレッションは Firefox 55 で `MSThemeCompatible` 対応を廃止することで解決されました。ウェブ開発者の皆さんは単純にサイトからこの時代遅れとなった `<meta>` タグを取り除くことで問題を回避できます。
