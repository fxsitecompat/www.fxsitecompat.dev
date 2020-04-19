---
title: "`RegExp.multiline` グローバルスイッチが廃止予定となりました"
date: "2015-12-19T00:43:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1220457"
      title: "Bug 1220457 - Show deprecation warning for non-standard RegExp.multiline."
---
新たな正規表現の複数行オプションを変更する、[`RegExp`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) オブジェクト上の非標準 `multiline` プロパティが廃止予定とされ、[近い将来削除されることとなりました](https://www.fxsitecompat.dev/ja/docs/2015/regexp-multiline-global-switch-will-be-removed/)。Firefox 46 以降、ウェブコンソールはこのプロパティに対する廃止警告を表示します。`RegExp` リテラルとコンストラクターの `m` フラグを代わりに使用してください。なお、`RegExp` インスタンス上の標準 [`multiline`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) プロパティは削除されません。

**更新**: このプロパティの対応は [Firefox 48 で削除されました](https://www.fxsitecompat.dev/ja/docs/2016/regexp-multiline-global-switch-has-been-removed/)。
