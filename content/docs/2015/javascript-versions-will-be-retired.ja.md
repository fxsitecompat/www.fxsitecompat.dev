---
title: "JavaScript のバージョンが撤廃されます"
date: "2015-10-26T17:40:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867609"
      title: "Bug 867609 - Retire JavaScript versions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867612"
      title: "Bug 867612 - Make sure JavaScript version is not used on the web"
---
Firefox では伝統的に、一部の最新 JavaScript 機能を利用するには [`<script>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/script) 要素でバージョンを明示する必要がありました。

```html
<script type="application/javascript;version=1.7"></script>
```

Firefox 44 以降、[`let`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let) 命令文は [明示的な JavaScript バージョンを必要としなくなり](https://www.fxsitecompat.com/ja/docs/2015/let-statement-no-longer-requires-explicit-javascript-version/)、この Firefox 固有のバージョニングはまもなく廃止されます。
