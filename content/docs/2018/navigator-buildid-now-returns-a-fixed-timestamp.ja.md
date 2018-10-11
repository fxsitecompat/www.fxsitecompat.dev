---
title: "`navigator.buildID` が固定タイムスタンプを返すようになりました"
date: "2018-10-10T03:44:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=583181"
      title: "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
aliases:
    - "/ja/docs/2015/navigator-buildid-will-be-removed/"
    - "/ja/docs/2018/navigator-buildid-has-been-removed/"
---
14 桁の数字から成る Firefox の識別子データを返す非標準の [`navigator.buildID`](https://developer.mozilla.org/docs/Web/API/Navigator/buildID) プロパティが `"20181001000000"` に固定されました。この変更はユーザープライバシー保護強化の一環として行われたものです。

[Firefox 16](https://www.fxsitecompat.com/ja/docs/2012/ua-string-no-longer-contains-patch-level-version-number/) 以降、マイナーバージョン番号は、`navigator.userAgent` プロパティや `User-Agent` HTTP ヘッダーで取得可能なブラウザーのユーザーエージェント (UA) 文字列から除外されています。また、[Firefox 25](https://www.fxsitecompat.com/ja/docs/2015/build-id-in-ua-string-is-now-frozen-at-20100101/) 以降、UA 文字列内のビルド ID は `20100101` に固定されています。しかしながら、`navigator.buildID` プロパティは Firefox のマイナーリリースやプラットフォームによって異なる実際のビルド ID を露呈し続けていて、これはフィンガープリンティング要因となる恐れがありました。

このプロパティは一部のウェブサイトでブラウザー判別のために使われている可能性があることから、ウェブコンテンツに対する非標準プロパティの露呈は理想的でないものの、削除される代わりに固定されることとなりました。

**更新**: この記事の初版ではプロパティが削除されたと記載していましたが、実際には潜在的な互換性問題を防ぐため残されています。タイトルと概要は修正済みです。
