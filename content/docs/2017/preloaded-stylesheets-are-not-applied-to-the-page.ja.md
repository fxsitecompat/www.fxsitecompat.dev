---
title: "先読みされたスタイルシートがページに適用されません"
date: "2017-10-24T19:10:00-04:00"
categories: ["css"]
tags: []
versions: ["56", "60-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405761"
      title: "Bug 1405761 - css not loaded correctly with rel=preload"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/aNUUx0S6PxE/discussion"
      title: "Intent to unship: rel=preload for firefox 57"
aliases:
    - "/ja/docs/2017/css-loaded-with-link-rel-preload-are-not-applied/"
---
ウェブパフォーマンス改善のため、`<link rel="preload">` による [コンテンツ先読み](https://developer.mozilla.org/docs/Web/HTML/Preloading_content) 対応が Firefox 56 で追加されました。ところが、先読みされた CSS スタイルシートが HTML ドキュメントへ正しく適用されないという報告が寄せられています。そのため、Mozilla 開発者が解決策に取り組んでいる間、この新機能は Firefox 57 で一時的に無効化され、2018 年 1 月公開の Firefox 58 で再度有効化される予定です。
