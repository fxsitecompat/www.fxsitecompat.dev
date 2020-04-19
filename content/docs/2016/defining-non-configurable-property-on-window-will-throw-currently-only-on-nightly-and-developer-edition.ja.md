---
title: "`window` 上での変更不能プロパティ定義が例外となります (今のところ Nightly と Developer Edition のみ)"
date: "2016-04-10T01:08:00-04:00"
categories: ["dom"]
tags: []
releases: ["42", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107443"
      title: "Bug 1107443 - Make WindowProxy throw if you attempt to define a non-configurable property"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1178638"
      title: "Bug 1178638 - Turn on the exceptions from bug 1107443 (Object.defineProperty on window with non-configurable property) on beta/release"
aliases:
    - "/ja/docs/2016/window-now-throws-when-defining-non-configurable-property-currently-only-on-nightly-and-developer-edition/"
---
Firefox 42 以降では、[`Object.defineProperty`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) あるいは [`Object.defineProperties`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperties) メソッドで [`window`](https://developer.mozilla.org/docs/Web/API/Window) 上に変更不能プロパティを定義しようとすると [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) が投げられます。今のところ、この変更は Firefox Nightly と Developer Edition のみで行われています。いくつかのサイト互換性問題が見つかっており、それを受けて Mozilla 開発者が次のステップを議論しています。
