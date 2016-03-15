---
title: "スクロール連動位置合わせは非同期スクロールと相性が悪い場合があり、コンソールに警告が表示されます"
date: "2016-01-07T09:01:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1229052"
      title: "Bug 1229052 - Log a warning if webpage is updating positioning properties during a scroll event listener"
    - url: "https://hacks.mozilla.org/2016/02/smoother-scrolling-in-firefox-46-with-apz/"
      title: "Mozilla Hacks - Smoother scrolling in Firefox 46 with APZ"
---
Firefox 46 以降、[`scroll`](https://developer.mozilla.org/ja/docs/Web/Events/scroll) イベントリスナー内でスクロール位置プロパティを変更しているページスクリプトに対し、Web コンソールが警告を表示するようになりました。そうしたイベントハンドラは、要素の固定、スクロールスナップ効果、あるいはパララックス効果に利用されることがしばしばありますが、Firefox に実装中の非同期スクロール機能と相性が悪い場合があります。詳細と考えられる回避策については、MDN の [Scroll-Linked Effects](https://developer.mozilla.org/ja/docs/Mozilla/Performance/ScrollLinkedEffects) ページを参照してください。
