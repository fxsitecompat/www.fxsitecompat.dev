---
title: "`scrollX`、`scrollY`、`pageXOffset`、`pageYOffset` が整数の代わりに浮動小数点数を返すようになりました"
date: "2017-03-18T22:09:00-04:00"
categories: ["dom"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1151421"
      title: "Bug 1151421 - Make window.pageYOffset/pageXOffset/scrollX/scrollY double, not integers"
---
Firefox 55 以降、`window` 上の [`scrollX`](https://developer.mozilla.org/docs/Web/API/Window/scrollX)、[`scrollY`](https://developer.mozilla.org/docs/Web/API/Window/scrollY) 両プロパティとそれらのエイリアスである [`pageXOffset`](https://developer.mozilla.org/docs/Web/API/Window/pageXOffset)、[`pageYOffset`](https://developer.mozilla.org/docs/Web/API/Window/pageYOffset) は、[`getBoundingClientRect`](https://developer.mozilla.org/docs/Web/API/Element/getBoundingClientRect) メソッドが返す値と同様に、サブピクセル精度を持つ浮動小数点数を返します。必要であれば、[`Math.round`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/round) メソッドを使って、それらを従来の整数値へキャストしてください。
