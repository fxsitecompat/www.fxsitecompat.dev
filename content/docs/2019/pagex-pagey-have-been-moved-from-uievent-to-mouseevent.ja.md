---
title: "`pageX`/`pageY` が `UIEvent` から `MouseEvent` へ移されました"
date: "2019-07-06T22:22:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1178763"
      title: "Bug 1178763 - TouchEvent.pageX/pageY should be undefined"
---
従来 `UIEvent` インターフェイス上で使用可能となっていた `pageX`、`pageY` プロパティが `MouseEvent` インターフェイスへ移動されました。理由は Firefox の実装が仕様に準拠していなかったためです。これにより両プロパティは、すべて `UIEvent` を継承している `CompositionEvent`、`FocusEvent`、`InputEvent`、`KeyboardEvent`、`TouchEvent` インターフェイスに露呈されなくなります。

[Google Chrome](https://groups.google.com/a/chromium.org/d/topic/blink-dev/pcMwyHRhbCU/discussion) は既にバージョン 45 で同様の変更を行っており、このバグ修正はウェブの相互運用性を向上させるはずです。
