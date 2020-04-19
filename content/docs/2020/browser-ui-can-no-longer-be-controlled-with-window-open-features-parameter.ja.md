---
title: "`window.open()` の機能引数によるブラウザー UI の制御が不可能となりました"
date: "2020-04-06T22:48:00-04:00"
categories: ["dom"]
tags: []
releases: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1507375"
      title: "Bug 1507375 - Can we drop window.open's feature parameter which controls UI parts visibility?"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/_3aWsRQ8Tfs/discussion"
      title: "Intent to ship: Restrict window.open features parameter"
---
ウェブ開発者は [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) メソッドのオプション引数 `windowFeatures` を使って新しいタブやウィンドウをどのようにユーザーに対して表示するかを定義することができます。ただし、この挙動は [実装依存](https://arai-a.github.io/window-open-features/) です。

Firefox 76 以降、`menubar`、`personalbar`、`toolbar` といった特定のウィンドウ機能を用いてブラウザーのユーザーインターフェイス要素を制御することはできなくなります。これらには Firefox と Internet Explorer しか対応していませんでした。今回の変更は、他のモダンブラウザーと整合性を高めることだけでなく、UI のカスタマイズやセッション復元による予期せぬ挙動を防ぐことを目的としています。

それらのウィンドウ機能は今後も、Firefox が新しいタブを開くか、あるいはポップアップウィンドウを開くかを決定するための [条件](https://hg.mozilla.org/mozilla-central/rev/bf0e49a9ceff#l9.12) として使用されます。
