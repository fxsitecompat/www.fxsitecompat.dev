---
title: "`getComputedStyle()` がスタイルを取得できない場合に `null` を返さないようになりました"
date: "2018-08-15T02:35:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1467722"
      title: "Bug 1467722 - Don't return null from getComputedStyle when there's no presentation."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1490688"
      title: "Bug 1490688 - Dropdown wrong position"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jh-HAAY1pAQ/discussion"
      title: "Slightly delayed Intent to Ship: getComputedStyle changes on some edge cases."
---
[`window.getComputedStyle`](https://developer.mozilla.org/docs/Web/API/Window/getComputedStyle) メソッドは従来、指定された要素のスタイルが取得できない場合に `null` を返すか例外を投げていました。こうしたエッジケースは例えば表示されていない `<iframe>` などで見られます。Firefox 62 以降、CSSOM 仕様や他のブラウザーの挙動との整合性を高めるため、このメソッドは、`length` プロパティに `0`、すべての宣言に空文字列を伴った `CSSStyleDeclaration` オブジェクトを返すようになります。

**更新**: この変更により *Zendesk Web Widget* に影響があり、ドロップダウンメニューが間違った位置に表示されています。
