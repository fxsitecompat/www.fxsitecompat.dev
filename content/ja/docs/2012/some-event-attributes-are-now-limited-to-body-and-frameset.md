---
title: "一部のイベント属性が `body`/`frameset` 要素専用になりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=809765"
      title: "Bug 809765 – Stop compiling the beforeunload attribute into an event handler on elements other than <body> and <frameset>"
---
従来、[`onbeforeunload`](https://developer.mozilla.org/ja/docs/DOM/window.onbeforeunload) 属性はどの要素に指定しても認識され、イベント発生時に指定したハンドラーが呼び出されていましたが、仕様に従って、[`body`](https://developer.mozilla.org/ja/docs/HTML/Element/body)、[`frameset`](https://developer.mozilla.org/ja/docs/HTML/Element/frameset) 以外の要素に指定した場合は無視されるようになりました。その他、[`onafterprint`](https://developer.mozilla.org/ja/docs/DOM/window.onafterprint)、[`onbeforeprint`](https://developer.mozilla.org/ja/docs/DOM/window.onbeforeprint)、[`onhashchange`](https://developer.mozilla.org/ja/docs/DOM/window.onhashchange)、`onoffline`、`ononline`、`onpagehide`、`onpageshow`、[`onpopstate`](https://developer.mozilla.org/ja/docs/DOM/window.onpopstate)、[`onresize`](https://developer.mozilla.org/ja/docs/DOM/window.onresize)、[`onunload`](https://developer.mozilla.org/ja/docs/DOM/window.onunload) 属性が同様の扱いとなりました。
