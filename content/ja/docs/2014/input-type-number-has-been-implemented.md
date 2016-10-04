---
title: "`<input type=\"number\">` が実装されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
versions: ["29"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=344616"
      title: "Bug 344616 – Implement <input type=\"number\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=946398"
      title: "Bug 950737 – Flip the pref to enable <input type=number>"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=947728"
      title: "Bug 947728 – Provide a way for content to hide <input type=number>\'s spinner"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1000400"
      title: "Bug 1000400 – skyscanner.com layout broken because site doesn\'t leave enough room for arrow buttons on <input type=\"number\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1008385"
      title: "Bug 1008385 – Betterment.com \"Goal set up\" page\'s funded-in-X-years input is broken, due to spinners pushing number out of view"
---
[`<input>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input) 要素が HTML5 で導入された `number` 形式に対応しました。この変更で矢印付きの増減ボタンが追加されたことによるリグレッションが少なくとも 2 件発見されています。ページ作者は、必要であれば CSS [`-moz-appearance: textfield`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-appearance) を使ってボタンを隠すことができます。これは仕様の一部ではありませんが、Chrome 用の `-webkit-appearance: none` と同様の挙動となります。
