---
title: "接頭辞付き CSS マルチカラムプロパティが廃止されました"
date: "2020-01-16T22:03:00-05:00"
categories: ["css"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308636"
      title: "Bug 1308636 - Remove support for -moz-prefixed CSS multi-column properties"
aliases:
    - "/ja/docs/2016/prefixed-css3-multi-column-properties-will-be-removed/"
---
[Firefox 52](https://www.fxsitecompat.dev/ja/docs/2016/css3-multi-column-properties-have-been-unprefixed/) 以降廃止予定となっていた以下の `-moz` 接頭辞付きマルチカラムプロパティへの対応が Firefox 74 で削除されました。代わりに標準の接頭辞なしプロパティを使用してください。

* `-moz-columns`
* `-moz-column-count`
* `-moz-column-fill`
* `-moz-column-gap`
* `-moz-column-rule`
* `-moz-column-rule-width`
* `-moz-column-rule-style`
* `-moz-column-rule-color`
* `-moz-column-span`
* `-moz-column-width`
