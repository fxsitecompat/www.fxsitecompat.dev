---
title: "`background-clip` と `background-origin` の対応が `background` ショートハンドプロパティへ追加されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["css"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=570896"
      title: "Bug 570896 - Add support for different background-origin and background-clip in background shorthand"
---
ここで起こり得る互換性の問題としては、[`background-origin`](https://developer.mozilla.org/ja/docs/Web/CSS/background-origin) あるいは [`background-clip`](https://developer.mozilla.org/ja/docs/Web/CSS/background-clip) が [`background`](https://developer.mozilla.org/ja/docs/Web/CSS/background) ショートハンドプロパティで明示的に指定されていなかった場合、それらは [初期値](https://developer.mozilla.org/ja/docs/Web/CSS/initial) にリセットされてしまいます。
