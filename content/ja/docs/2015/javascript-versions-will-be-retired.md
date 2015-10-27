---
title: "JavaScript のバージョンが撤廃されます"
date: "2015-10-26T17:40:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=855665": "Bug 855665 - Enable let without version=1.7+"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=867609": "Bug 867609 - Retire JavaScript versions"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=867612": "Bug 867612 - Make sure JavaScript version is not used on the web"
---
Firefox では伝統的に、一部の最新 JavaScript 機能を利用するには [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) 要素でバージョンを明示する必要がありました。

```html
<script type="application/javascript;version=1.7"></script>
```

ECMAScript 2015 (ES6) で標準化された [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) 命令文はまもなく `version=1.7` 以降のバージョンがなくても使えるようになり、この Firefox 固有のバージョニングは廃止されます。
