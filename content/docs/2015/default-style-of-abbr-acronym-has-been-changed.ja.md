---
title: "`<abbr>`/`<acronym>` の既定のスタイルが変更されました"
date: "2015-04-27T13:17:23-04:00"
categories: ["css"]
tags: []
versions: ["40"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1157083"
      title: "Bug 1157083 - It might be better to use CSS3 text-decoration for the UA stylesheet of <abbr> and <acronym> rather than border-bottom"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6FETMqsuQhk/discussion"
      title: "mozilla.dev.platform: Intent to change UA stylesheet of <abbr> and <acronym> (using border-bottom -> CSS 3 text-decoration)"
---
Firefox のユーザーエージェントスタイルシートが更新され、[`<abbr>`](https://developer.mozilla.org/docs/Web/HTML/Element/abbr)、[`<acronym>`](https://developer.mozilla.org/docs/Web/HTML/Element/acronym) 要素に CSS3 の [`text-decoration`](https://developer.mozilla.org/docs/Web/CSS/text-decoration) プロパティが使われるようになりました。具体的には、`border-block-end: dotted 1px` が `text-decoration: dotted underline` に置き換えられました。あなたのサイトでこれらの要素のいずれかに独自のスタイルを適用している場合、それが UA スタイルシートと競合していないか確認した方が良いでしょう。なお、Google Chrome はまだ `text-decoration` ではなく [`border-bottom`](https://developer.mozilla.org/docs/Web/CSS/border-bottom) を使用していますので、これらの要素へ意図した通りのスタイルを適用するには両方のプロパティを使い続ける必要があります。

現在のところ、[*Bootstrap*](https://github.com/twbs/bootstrap/issues/16574) と [*Normalize.css*](https://github.com/necolas/normalize.css/pull/451) がこの変更の影響を受けることが判明しています。それらの開発者は回避策に取り組んでおり、各ライブラリのユーザーはコードを更新する必要があるでしょう。
