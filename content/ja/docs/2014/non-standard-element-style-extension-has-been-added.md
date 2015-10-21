---
title: "非標準 `element.style` 拡張が実装されました"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=958887": "Bug 958887 – Add support for element.style[\"css-property-name\"] non-standard extension"
---
`element.style["css-property-name"]` のような単純な構文で CSS プロパティの取得と設定を可能にする、[`HTMLElement.style`](https://developer.mozilla.org/ja/docs/Web/API/HTMLElement.style) プロパティの非標準拡張が Firefox でも使用可能となりました。他のすべての主要ブラウザがこの形式に対応しているため、相互運用性の向上が見込まれます。
