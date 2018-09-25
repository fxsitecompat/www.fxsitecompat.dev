---
title: "`navigator.buildID` が削除されます"
date: "2015-10-25T21:43:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=583181"
      title: "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
---
Firefox のビルド識別子を返す非標準の [`navigator.buildID`](https://developer.mozilla.org/docs/Web/API/Navigator/buildID) プロパティを、ユーザープライバシー保護のため削除することが検討されています。この 14 桁の数字から成る識別子データがフィンガープリンティングに使われる可能性があるためです。

[Firefox 16](https://www.fxsitecompat.com/ja/docs/2012/ua-string-no-longer-contains-patch-level-version-number/) 以降、マイナーバージョン番号は、`navigator.userAgent` プロパティで取得可能なブラウザーのユーザーエージェント (UA) 文字列から除外されています。また、[Firefox 25](https://www.fxsitecompat.com/ja/docs/2015/build-id-in-ua-string-is-now-frozen-at-20100101/) 以降、UA 文字列内のビルド ID は `20100101` に固定されています。しかしながら、`navigator.buildID` プロパティは未だに Firefox のマイナーリリースやプラットフォームによって異なる実際のビルド識別子を露呈しており、これはフィンガープリンティング要因になる恐れがあります。

**更新**: Mozilla のエンジニアは Firefox 64 でこのプロパティを廃止することを予定しています。
