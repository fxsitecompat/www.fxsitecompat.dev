---
title: "UA 文字列内の Gecko ビルド日付がバージョン番号に置き換えられました"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: "17"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=588909": "Bug 588909 – Replace Gecko/<date> with Gecko/<version> in UA string"
---
ユーザエージェント (UA) 文字列のうち、Firefox のレンダリングエンジンである [Gecko](https://developer.mozilla.org/ja/docs/Gecko) の表記が変わりました。[Firefox 4](https://hacks.mozilla.org/2010/09/final-user-agent-string-for-firefox-4/) 以降固定されているビルド日時がバージョン番号に置き換えられました。このため `Gecko/20100101` が `Gecko/17.0` となります。ユーザエージェント文字列からブラウザのバージョン判別を行っている場合は注意が必要です。

<ins datetime="2012-11-30">11/30 更新: この変更はサイト互換性に及ぼす影響が大きいと思われることから、[Firefox 17.0.1 でバックアウトされました](https://bugzilla.mozilla.org/show_bug.cgi?id=815743)。</ins>
