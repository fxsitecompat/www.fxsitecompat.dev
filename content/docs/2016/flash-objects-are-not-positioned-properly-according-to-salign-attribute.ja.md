---
title: "Flash オブジェクトが `salign` 属性に従って適切に配置されません"
date: "2016-10-24T10:41:00-04:00"
categories: ["plugins"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307694"
      title: "Bug 1307694 - Flash objects in Firefox 49 are not positioned according to the salign attribute"
---
`<object>`、`<embed>` 両要素のための `salign` [オプション属性](https://helpx.adobe.com/flash/kb/flash-object-embed-tag-attributes.html#main_Optional_attributes) が無視され、特定の Flash オブジェクト内で予期せぬレイアウトにつながるというリグレッションが Firefox 49 で発生しました。このバグは Firefox 50 で修正されました。
