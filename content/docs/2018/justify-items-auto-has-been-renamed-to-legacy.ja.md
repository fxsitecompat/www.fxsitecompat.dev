---
title: "`justify-items:auto` が `legacy` へ改名されました"
date: "2018-05-07T19:25:00-04:00"
categories: ["css"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1363875"
      title: "Bug 1363875 - [css-align] Rename `auto` to `legacy` for `justify-items`"
---
従来、[`justify-items`](https://developer.mozilla.org/docs/Web/CSS/justify-items) CSS プロパティの初期値は `auto` でした。 CSS ワーキンググループ内での [議論](https://github.com/w3c/csswg-drafts/issues/1318) の結果、これは `legacy` に改名されました。Firefox 61 は最新の Box Alignment 仕様に従ってこの変更を行い、移行期間なしに `auto` を不正値としました。今後は `legacy` を代わりに使ってください。
