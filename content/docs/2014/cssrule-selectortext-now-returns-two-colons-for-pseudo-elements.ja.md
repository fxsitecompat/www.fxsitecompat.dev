---
title: "`CSSRule.selectorText` が疑似要素にコロンを 2 つ付けて返すようになりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
versions: ["36"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949651"
      title: "Bug 949651 – Pseudo-elements should always be separated by two colons in selectorText"
---
[`::before`](https://developer.mozilla.org/docs/Web/CSS/::before)、[`::after`](https://developer.mozilla.org/docs/Web/CSS/::after)、[`::first-letter`](https://developer.mozilla.org/docs/Web/CSS/::first-letter)、[`::first-line`](https://developer.mozilla.org/docs/Web/CSS/::first-line) の各疑似要素が、[`CSSStyleRule.selectorText`](https://developer.mozilla.org/docs/Web/API/CSSStyleRule/selectorText) CSSOM プロパティでアクセスした場合に、CSS3 仕様で定義されている通り 2 つのコロン (`::`) 付きで返されるようになりました。従来このプロパティは CSS2 のシングルコロン (`:`) 構文でこれらの疑似要素を返していました。
