---
title: "特定のマルチカラムレイアウトで、バランスが崩れたり、ランダムに要素が欠落する場合があります"
date: "2017-11-10T03:24:00-05:00"
categories: ["css"]
tags: []
versions: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308876"
      title: "Bug 1308876 - Nested inline-blocks with matching width locks up browser due to O(2^depth) reflow performance"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406619"
      title: "Bug 1406619 - Two-column layout balanced unevenly and nondeterministically since Firefox 56"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1411799"
      title: "Bug 1411799 - Content of ::before/after pseudo elements randomly disappears when display:inline-block and float are used"
---
あるパフォーマンス改善が原因で、[CSS マルチカラムレイアウト](https://developer.mozilla.org/docs/Web/CSS/CSS_Columns) に関するリグレッションが Firefox 56 で発生しました。ひとつの報告では 2 列のレイアウトが不均衡になってしまうことが示されています。別のバグは皮肉にもこの [FxSiteCompat.com](https://www.fxsitecompat.dev/ja/docs/) 上で見つかり、マルチカラムレイアウトが `display:inline-block` や `float:left` と組み合わされた場合、内部の `::before` 疑似要素がランダムに消えてしまいます。厄介なことに、いずれの場合も挙動が気まぐれです。Mozilla 開発者がじきに問題を調査します。

**更新**: このバグは Firefox 70 で修正されました。
