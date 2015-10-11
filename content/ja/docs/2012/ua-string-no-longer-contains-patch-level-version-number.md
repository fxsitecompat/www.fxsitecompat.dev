---
title: "UA 文字列にパッチレベルのバージョン番号まで含まれなくなります"
date: "2012-10-09T06:00:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=728831": "Bug 728831 – Don’t expose the Firefox patch level (13.X.Y) in the UA string, only show the major version (13.X)"
---
フィンガープリンティングのリスクを緩和するため、[Firefox のユーザエージェント (UA) 文字列](https://developer.mozilla.org/ja/docs/Web/HTTP/Gecko_user_agent_string_reference) にセキュリティパッチレベルのバージョン番号が露呈されなくなりました。そのため、例えば予定外の Firefox 16.0.1 がリリースされた場合も、UA 文字列内のバージョンは `16.0.1` ではなく`16.0` とだけ表記されます。
