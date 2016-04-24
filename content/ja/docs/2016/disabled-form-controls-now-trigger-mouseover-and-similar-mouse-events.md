---
title: "無効化されているフォームコントロール上で `mouseover` や同様のマウスイベントが発生するようになりました"
date: "2016-04-23T23:51:00-04:00"
categories: ["dom"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=218093"
      title: "Bug 218093 - disabled child element doesn't produce mouseout/mouseover pair"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1265909"
      title: "Bug 1265909 - FireFox 45.0.2 fires onMouseOut for disabled input."
---
Firefox 44 以降、[`mouseover`](https://developer.mozilla.org/ja/docs/Web/Events/mouseover)、[`mouseout`](https://developer.mozilla.org/ja/docs/Web/Events/mouseout)、[`mouseenter`](https://developer.mozilla.org/ja/docs/Web/Events/mouseenter)、[`mouseleave`](https://developer.mozilla.org/ja/docs/Web/Events/mouseleave) の各イベントが、[`<input>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input) などの無効化されているフォームコントロール上でも発生するようになりました。従来の挙動は特に jQuery を使っている Web 開発者を混乱させることがありました。

あなたのコードが常に期待通り動作するよう、イベントハンドラ内でターゲット要素の `disabled` プロパティを明示的に確認すると良いでしょう。
