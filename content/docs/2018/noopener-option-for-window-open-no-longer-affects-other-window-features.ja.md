---
title: "`window.open()` の `noopener` オプションが他のウィンドウ特性に影響しなくなりました"
date: "2018-08-16T09:27:00-04:00"
categories: ["dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1419960"
      title: "Bug 1419960 - Make the noopener window feature not affect whether other window features are enabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6cTk_b1l6LE/discussion"
      title: "Intent to ship: Change the effect of noopener window feature on other window features in window.open"
---
これまで、`window.open(url, '_blank', 'noopener')` は、他の [ウィンドウ特性](https://developer.mozilla.org/docs/Web/API/Window/open#Window_features) が無効化され、タブや戻る・進むボタンが非表示となった新たなブラウザーウィンドウを開いていました。

これはユーザーにとって予期せぬ挙動と思われることから、Firefox 63 以降ではそうしたコードが `window.open(url, '_blank')` と同様に扱われ、すべてのウィンドウ特性が有効となった新しいブラウザータブが開かれます。唯一の違いは新しいタブの `window.opener` プロパティが `null` となることです。

何らかのウィンドウ特性が必要な場合、`noopener` と併せて明示的にそれらのオプションを指定してください。
