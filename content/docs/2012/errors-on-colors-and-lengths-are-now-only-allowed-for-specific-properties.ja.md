---
title: "色や長さに関する誤記の許容が特定のプロパティに制限されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["css"]
tags: []
versions: ["17"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=774122"
      title: "Bug 774122 – limit CSS parser hashless-color and unitless-length quirks to only the properties that need them"
---
Firefox の [Quirks (後方互換) モード](https://developer.mozilla.org/ja/docs/Mozilla_Quirks_Mode_Behavior) では、ハッシュの付いていないカラーコード (例えば `#666666` の誤記である `666666`) や、単位の付いていない長さ (例えば `10px` の誤記である `10`) がショートハンド以外のプロパティの値に見つかった場合、CSS パーサーによって自動的に補正されます。CSS3 の仕様に合わせて、特定のプロパティに限ってそうした誤記を許容する実装に変更されました。

例えばハッシュなしカラーコードの場合、許容範囲は [`background-color`](https://developer.mozilla.org/ja/docs/CSS/background-color)、[`border-color`](https://developer.mozilla.org/ja/docs/CSS/border-color)、[`border-top-color`](https://developer.mozilla.org/ja/docs/CSS/border-top-color)、[`border-right-color`](https://developer.mozilla.org/ja/docs/CSS/border-right-color)、[`border-bottom-color`](https://developer.mozilla.org/ja/docs/CSS/border-bottom-color)、[`border-left-color`](https://developer.mozilla.org/ja/docs/CSS/border-left-color)、[`color`](https://developer.mozilla.org/ja/docs/CSS/color) プロパティの値のみであり、[`background`](https://developer.mozilla.org/ja/docs/CSS/background) や [`border`](https://developer.mozilla.org/ja/docs/CSS/border) など他のプロパティの値に含まれる誤記は補正されません。いずれにしても誤記は自分自身で修正するようにしましょう。
