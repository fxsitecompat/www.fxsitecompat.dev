---
title: "`document.referrer` の実装が最新仕様に合わせて更新されました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=809290"
      title: "Bug 809290 – document.referrer should be based on the script entry point"
---
入れ子になったインラインフレーム (`iframe`) や孫ウィンドウの URL が親ウィンドウから動的に変更された場合、[`document.referrer`](https://developer.mozilla.org/docs/DOM/document.referrer) プロパティの値が、直接参照元の子ウィンドウではなく、スクリプトの書かれている親ウィンドウの URL を指すようになりました。これは仕様変更によるもので、Internet Explorer や Opera と同じ挙動になり、WebKit も追従する見込みです。
