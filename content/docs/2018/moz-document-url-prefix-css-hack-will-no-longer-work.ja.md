---
title: "`@-moz-document url-prefix()` CSS ハックは使えなくなります"
date: "2018-06-05T17:57:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449753"
      title: "Bug 1449753 - Turn off layout.css.moz-document.url-prefix-hack.enabled by default."
---
CSS インジェクション攻撃のリスクを軽減するため、[`@-moz-document`](https://developer.mozilla.org/docs/Web/CSS/@document) CSS アットルールは [Firefox 61 で無効化](https://www.fxsitecompat.com/ja/docs/2018/moz-document-support-has-been-dropped-except-for-empty-url-prefix/) されましたが、空の `url-prefix` 関数は、[Firefox を対象とした CSS ハック](https://css-tricks.com/snippets/css/css-hacks-targeting-firefox/) として使われていることが分かっているため、引き続きパースされています。

```css
/* これは Firefox でのみ動作します */
@-moz-document url-prefix() {
  #prices td {
    height: 100%;
  }
}
```

セキュリティへの懸念から、いずれにせよこの残りの対応も、近い将来主な互換性問題が解決したら廃止されます。もしあなたがこのハックを使って Firefox の特定のレイアウトバグを回避している場合は、[Bugzilla へ問題を報告](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Layout&blocked=1449753) するか [私たちに知らせてください](https://www.fxsitecompat.com/ja/contribute/)。
