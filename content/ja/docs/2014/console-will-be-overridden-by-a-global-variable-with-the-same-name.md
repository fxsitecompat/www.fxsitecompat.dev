---
title: "`console` が同名のグローバル変数によって上書きされてしまいます "
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: []
versions: "30"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=965860": "Bug 965860 – Rewrite ConsoleAPI in C++"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1024806": "Bug 1024806 – Ro.me does not load after clicking the try anyway warning. Worked in ff29."
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1024899": "Bug 1024899 – After update from v 29.0.1 to v 30.0 the site: https://home.cgm-life.de/fb363286-e393-4a31-84c1-9c60e07c6cef cannot be reached (responsive design - twitter bootstrap - Angular JS)"
---
[`console`](https://developer.mozilla.org/ja/docs/Web/API/console) の新しい実装が原因で、`console` という名前のユーザ定義グローバル変数が存在する場合、それによってこのオブジェクトが上書きされ、結果として予期せぬ挙動が発生してしまいます。少なくとも 2 つのサイトが正しく動作しなくなっていることが判明しており、いずれもトップレベルのコードで `var console` が定義され、その後 [`console.log`](https://developer.mozilla.org/ja/docs/Web/API/console.log) が呼び出されています。Firefox 31 以降のバージョンは別の実装変更のおかげで影響を受けません。
