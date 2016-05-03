---
title: "CSS `perspective` と `z-index` の組み合わせが間違った重ね順になります"
date: "2016-05-03T14:05:00-04:00"
categories: ["css"]
tags: []
versions: ["46"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269184"
      title: "Bug 1269184 - CSS perspective and z-index not layered properly on Firefox 46+, breaking site navigation on ESPN FC and ADS-B Exchange"
---
CSS [`perspective`](https://developer.mozilla.org/ja/docs/Web/CSS/perspective)、[`z-index`](https://developer.mozilla.org/ja/docs/Web/CSS/z-index) 両プロパティでスタイル付けされた HTML 要素が正しい重ね順で描画されず、例えばサイトナビゲーションが見えなくなる状態を引き起こすというリグレッションが Firefox 46 で発生しました。*ESPN FC* やその他のサイトが影響を受けています。Mozilla 開発者が解決策に取り組んでいます。
