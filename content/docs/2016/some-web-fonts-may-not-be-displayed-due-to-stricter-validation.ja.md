---
title: "一部のウェブフォントがより厳格なバリデーションのため表示されなくなる場合があります"
date: "2016-02-03T13:19:00-05:00"
categories: ["misc"]
tags: []
versions: ["44", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244693"
      title: "Bug 1244693 - FF 44 fails to load some WOFF fonts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331797"
      title: "Bug 1331797 - Can't load fonts on https://fonts.google.com/"
---
Firefox 44 以降で、OpenType Sanitizer の新バージョンによるより厳密なバリデーションが行われるため、一部のウェブフォントが拒絶される場合があります。仕様に反した OpenType レイアウトテーブルを含むフォントは描画されず、ウェブコンソールにそのエラーに関する警告が表示されます。

**更新**: *Nokia* を含め一部のサイトが影響を受けていることから、Firefox 45 以降、Beta、Release 両チャンネルではこのバリデーションは緩和されています。しかし、問題のあるフォントはいずれにしても置き換えられるべきです。

**更新 2**: [*Google Fonts*](https://fonts.google.com/) 上の一部フォントも壊れており、Firefox Nightly および Developer Edition では「豆腐」文字が表示されてしまいます。

**更新 3**: *Google Fonts* 上で正常に表示されなかったフォントは Google によって 2017 年 10 月に修正されました。
