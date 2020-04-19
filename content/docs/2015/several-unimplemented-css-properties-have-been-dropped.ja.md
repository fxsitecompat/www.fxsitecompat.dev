---
title: "いくつかの未実装 CSS プロパティが削除されました"
date: "2015-10-20T16:23:00-07:00"
categories: ["css"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215702"
      title: "Bug 1215702 - remove backend-only CSS properties (marks, orphans, page, size, widows)"
---
[`marks`](https://developer.mozilla.org/docs/Web/CSS/%40page/marks)、[`orphans`](https://developer.mozilla.org/docs/Web/CSS/orphans)、`page`、`size`、[`widows`](https://developer.mozilla.org/docs/Web/CSS/widows) 各プロパティへの対応が削除されました。これらはパース、キャッシュされていましたが、Firefox には実際にはまだ実装されていないため計算されていませんでした。[`@supports`](https://developer.mozilla.org/docs/Web/CSS/@supports) アットルールと [`CSS.supports`](https://developer.mozilla.org/docs/Web/API/CSS/supports) メソッドがこれらのプロパティに対応しなくなりますが、それ以外の点に関してこの変更はサイト互換性に影響しないはずです。
