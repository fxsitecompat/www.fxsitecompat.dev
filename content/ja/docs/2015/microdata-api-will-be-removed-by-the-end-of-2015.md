---
title: "Microdata API は 2015 年末までに廃止されます"
date: "2015-10-25T16:27:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=909633": "Bug 909633 - Remove HTML Microdata API"
---
[Microdata API](http://www.w3.org/TR/microdata/) は Firefox 16 で実装されましたが (その際に [サイト互換性問題を引き起こしています](https://www.fxsitecompat.com/en-US/docs/2012/microdata-api-has-added-new-properties-to-elements/))、後に HTML5 仕様から削除され、今のところ他のどのブラウザにも実装されていません。そのため、Mozilla 開発者は 2015 年第 4 四半期に API 対応を削除する計画を立てています。Web 開発者は、[Schema.org](https://schema.org/) などのマイクロデータを取得、操作するためにこの API を使用するのを避けるべきです。
