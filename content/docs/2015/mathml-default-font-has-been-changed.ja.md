---
title: "MathML の既定フォントが変更されました"
date: "2015-06-13T15:20:46-04:00"
categories: ["misc"]
tags: []
versions: ["41"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=947654"
      title: "Bug 947654 - Default fonts for MathML"
---
[MathML](https://developer.mozilla.org/docs/Web/MathML) フォントファミリー名がユーザーエージェントスタイルシート内にハードコードされなくなり、Firefox ユーザーは新しい `font.name.serif.x-math` 設定項目を変更して [任意のフォント](https://developer.mozilla.org/docs/Mozilla/MathML_Project/Fonts) を使用できるようになりました。MathJax と STIX General を含む旧来のフォントは非推奨となり、新たな主要フォールバックフォントとして Latin Modern Math が指定されました。
