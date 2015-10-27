---
title: "UA 文字列内のビルド ID が `20100101` に固定されました"
date: "2015-10-27T01:35:00-07:00"
categories: ["dom", "networking", "privacy-security"]
tags: []
versions: ["25"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=728773": "Bug 728773 - Always freeze the build ID in the UA string at 20100101"
    "https://developer.mozilla.org/ja/docs/Gecko_user_agent_string_reference": "Gecko ユーザエージェント文字列リファレンス"
---
HTTP `User-Agent` リクエストヘッダや、[`navigator.userAgent`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorID/userAgent)、[`navigator.productSub`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/productSub) 各 DOM プロパティを通じて取得できる Firefox のビルド識別子が、ブラウザのフィンガープリンティングの可能性を下げるため、`20100101` に固定されました。[`navigator.buildID`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/buildID) は引き続き正確なビルド識別子を返しますが、このプロパティを [将来的に削除する](https://www.fxsitecompat.com/ja/docs/2015/navigator-buildid-will-be-removed/) ことも検討されています。
