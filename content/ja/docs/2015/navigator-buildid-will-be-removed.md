---
title: "`navigator.buildID` が削除されます"
date: "2015-10-25T21:43:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=583181": "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
---
Firefox のビルド識別子を返す非標準の [`navigator.buildID`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/buildID) プロパティを、ユーザプライバシー保護のため削除することが検討されています。この 14 桁の数字から成る識別子データがフィンガープリンティングに使われる可能性があるためです。
