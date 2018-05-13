---
title: "`let` 命令文が明示的な JavaScript バージョンを必要としなくなりました"
date: "2015-10-28T02:02:00-07:00"
categories: ["javascript"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=855665"
      title: "Bug 855665 - Enable let without version=1.7+"
aliases:
    - "/ja/docs/2015/let-statement-no-longer-requires-explicit-javascript-version-in-non-strict-mode/"
---
これまで [`let`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let) 命令文は、以下の例のように、[`<script>`](https://developer.mozilla.org/docs/Web/HTML/Element/script) 要素上に明示的な JavaScript のバージョン、具体的には [1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) 以降を必要としていました。

```html
<script type="application/javascript;version=1.7"></script>
```

`let` 命令文は ECMAScript 2015 (ES6) で標準化されたため、そうしたバージョンを指定しなくても使えるようになりました。この変更は後方互換なはずですが、何か問題を見つけた場合は [お知らせください](https://www.fxsitecompat.com/ja/contribute/)。非標準の JavaScript バージョニングは近い将来 [完全に廃止されます](https://www.fxsitecompat.com/ja/docs/2015/javascript-versions-will-be-retired/)。
